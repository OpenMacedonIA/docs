# Retos de Desarrollo y Soluciones

Documentación de obstáculos técnicos y soluciones de ingeniería de bajo nivel.

## 1. Audio y Latencia

### Problema: PulseAudio en Headless
* **Impacto:** Latencia variable 200-500ms, consumo CPU.
* **Solución:** Migración a **ALSA** directo con `PyAudio`. Acceso exclusivo a hardware.
* **Resultado:** Latencia < 50ms.

### Problema: Eco
* **Impacto:** El micrófono capta la respuesta del TTS.
* **Solución:** "Semáforo de Audio". Mutear input durante estado `SPEAKING`.

## 2. Inteligencia Artificial

### Problema: Inferencia Lenta
* **Solución:** Uso de **Gemma-2B** y cuantización **GGUF** (Q4_K).
* **Resultado:** 4-6 tokens/seg en un RPi 4.

### Problema: Alucinaciones
* **Solución:** Prompt del sistema estricto y configuración de "Stop Tokens".

## 3. Sistema

### Problema: OOM Killer (Memoria)
* **Impacto:** Crash del proceso Python al cargar modelos.
* **Solución:** Carga diferida (Lazy Loading) y **ZRAM** (Swap comprimida en RAM).

### Problema: Corrupción SD
* **Solución:** Logs en RAM (`tmpfs`) y modo WAL en SQLite.
