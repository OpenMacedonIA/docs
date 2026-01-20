# Manual Técnico de Despliegue (Ingeniería)

**Proyecto:** NEOPapaya (Language Copilot for Group and Administration Environments) 
**Nivel de Acceso:** Ingeniería / DevOps

---

## 1. INTRODUCCIÓN TÉCNICA

### 1.1. Propósito
Este documento detalla la **ingeniería subyacente** del sistema. Está diseñado para ingenieros de DevOps, SREs (Site Reliability Engineers) y desarrolladores *backend*.

### 1.2. Stack Tecnológico Detallado
* **Lenguaje Core:** Python 3.10+ (Uso extensivo de `asyncio` para I/O bound y `threading` para CPU bound).
* **Inferencia LLM:** `llama.cpp` (vía `llama-cpp-python`) con soporte para instrucciones vectoriales AVX2/AVX512.
* **Audio I/O:** `PyAudio` interactuando directamente con ALSA.
* **STT Engine:** Vosk y Sherpa-ONNX.
* **TTS Engine:** Piper (neuronal rápido).
* **Vector Database:** ChromaDB.
* **NL2Bash Engine:** MANGO T5.
* **Bus de Eventos:** MQTT v3.1.1 (Mosquitto).
* **Base de Datos:** SQLite 3 (WAL).

---

## 2. ARQUITECTURA INTERNA Y FLUJO DE DATOS

### 2.1. Pipeline de Audio
1. **Captura:** `PyAudio` abre un stream directo al dispositivo `hw:X,Y`.
2. **VAD:** Energía (RMS) para detección rápida.
3. **Buffer:** `RingBuffer` para evitar underruns.

### 2.2. Esquema de Mensajería MQTT
**Topic Base:** `tio/agents/{hostname}/{type}`

| Nivel | Valor | Descripción |
| :--- | :--- | :--- |
| Root | `tio` | Namespace global. |
| Group | `agents` | Subgrupo. |
| ID | `{hostname}` | ID único. |
| Type | `telemetry` | Datos periódicos. |
| Type | `alerts` | Eventos críticos. |
| Type | `commands` | Comandos remotos. |

### 2.3. Gestión de Memoria
* **Carga Perezosa:** Modelos cargados bajo demanda.
* **Garbage Collection:** `gc.collect()` forzado.

---

## 3. INSTALACIÓN DE BAJO NIVEL

### 3.1. Compilación de Dependencias
Ciertas librerías requieren compilación específica (NEON en ARM, AVX en x86).

**Llama-cpp-python (Ejemplo RPi):**
```bash
CMAKE_ARGS="-DGGML_NEON=on" pip install llama-cpp-python --force-reinstall --no-cache-dir
```

### 3.2. Despliegue de Modelos
* **GGUF (Gemma):** Mapeado en memoria (`mmap`).
* **ONNX:** Optimizado con `onnxruntime`.

---

## 4. TUNING Y OPTIMIZACIÓN

### 4.1. Parámetros Sysctl
Añadir a `/etc/sysctl.d/99-neo-latency.conf`:
```ini
dev.hpet.max-user-freq = 2048
vm.swappiness = 10
net.core.rmem_max = 16777216
net.ipv4.tcp_fastopen = 3
```

### 4.2. Prioridad de Procesos
En `neo.service`:
```ini
CPUSchedulingPolicy=rr
CPUSchedulingPriority=50
Nice=-10
```

---

## 5. INFRAESTRUCTURA COMO CÓDIGO (IaC)

### 5.1. Dockerfile de Referencia
Utiliza *multi-stage builds*.
```dockerfile
FROM python:3.10-slim-bookworm AS builder
# ... (build dependencies)
FROM python:3.10-slim-bookworm
# ... (runtime dependencies)
CMD ["python", "start_services.py"]
```

### 5.4. Estrategia de Persistencia
* **Config**: ConfigMap/Read-only volume.
* **Database**: PVC/LocalPath.
* **Models**: Volumen compartido.

---

## 6. SEGURIDAD Y HARDENING

### 6.1. Aislamiento (Systemd)
```ini
ProtectHome=read-only
PrivateTmp=true
NoNewPrivileges=true
```

### 6.3. Fail2Ban
Configurar Jail para SSH para bloquear ataques de fuerza bruta.

---

## 7. ANEXOS TÉCNICOS

### 7.1. Mapa de Memoria (Estimado)
* **Idle:** ~350 MB
* **Load (Gemma + Whisper):** ~2.3 GB
* **Notas:** Requiere Swap en dispositivos de 2GB RAM.
