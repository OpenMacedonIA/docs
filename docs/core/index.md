# Arquitectura del Sistema (NEOPapaya v3.0 / Core v4)
*Combinación de Arquitectura Core y MANGO AI*

## ️ Visión General

NEOPapaya sigue una arquitectura **modular y orientada a eventos**, optimizada para ejecutarse en hardware de recursos limitados (Dual Core CPUs, 8GB RAM).

### Componentes Principales

1. **NeoCore (`NeoCore.py`)**:
    * **Función**: Orquestador central. Gestiona el ciclo de vida de la aplicación.
    * **Threading**: Utiliza hilos ligeros para manejar tareas simultáneas (Voz, Eventos, Web).
    * **V4 Optimization**: Implementa un **Watchdog** interno que supervisa y reinicia hilos críticos si fallan, garantizando "Alta Disponibilidad" local.

2. **Web Admin (`modules/web_admin.py`)**:
    * **Función**: Servidor API y Web Interface.
    * **Tecnología**: Flask + Flask-SocketIO.
    * **Aislamiento**: Se ejecuta en su propio hilo dentro de NeoCore, sirviendo la UI independientemente del estado de la IA.

3. **Managers (Decoupled Modules)**:
    * `VoiceManager`: Captura de audio y STT (Vosk/Whisper).
    * `MangoManager`: Inferencia de LLM especializado (T5) para comandos Bash. *Nota: Limitado a 1 hilo en V4 para no saturar CPU.*
    * `AIEngine`: Inferencia de LLM general (Gemma 2B) con `llama-cpp-python`.
    * `HealthManager`: Monitorización de servicios del sistema operativo (cron, docker, etc.).
    * **Advanced Modules**:
        * `Guard`: IDS basado en reglas y logs.
        * `CastManager`: Gestión de audio multi-habitación (Google Cast).
        * `Brain`: Gestión de memoria episódica y DB (SQLite).

## Flujo de Datos

1. **Input**: El usuario habla -> `VoiceManager` detecta y transcribe.
2. **Routing**: `NeoCore.handle_command` decide:
    * Es un comando de sistema? -> `MangoManager` (T5).
    * Es una charla? -> `AIEngine` (Gemma).
    * Es una orden directa? -> `IntentManager` (Reglas/Vosk).
3. **Ejecución**: El Manager correspondiente ejecuta la acción y devuelve texto.
4. **Output**: `Speaker` sintetiza la respuesta (TTS Piper) y `WebAdmin` actualiza la UI vía WebSocket.

## Optimizaciones Core V4 (Hardware Limitado)

Para funcionar fluidamente en un i3 7th Gen:

* **PyTorch Single-Thread**: Se fuerza a PyTorch (usado por Mango T5) a usar 1 solo hilo físico. Esto previene que la inferencia de la IA bloquee el procesamiento de audio en tiempo real.
* **Garbage Collection Forzada**: Se llama explícitamente al recolector de basura de Python tras la carga de modelos pesados (2GB+) para desfragmentar la RAM.
* **Lazy Loading**: Módulos pesados como `VisionManager` (OpenCV) solo se cargan si están habilitados en la configuración, evitando el consumo de memoria en reposo.

## ️ Seguridad

* **Web**: Cabeceras estrictas (CSP, HSTS) en el servidor interno Flask.
* **Ejecución**: Comandos generados por IA (Mango) pasan por un filtro de riesgo antes de ejecutarse. Comandos destructivos (`rm`, `mkfs`) requieren confirmación de voz explícita.

---

# MANGO: Documentación Técnica del Asistente Sysadmin AI (Detalle)

## 1. Introducción y Objetivos

El proyecto **MANGO** tiene como objetivo desarrollar un Modelo de Lenguaje Pequeño (SLM) especializado en administración de sistemas Linux.

### 1.1. El Problema
Los modelos generalistas sufren de "verborrea conversacional" (chatty behavior) y alucinaciones técnicas. Un Sysadmin necesita un motor de traducción **Lenguaje Natural -> Bash** estricto, sin saludos ni explicaciones superfluas.

## 2. Arquitectura del Modelo

### 2.1. Selección del Modelo: Salesforce CodeT5
Se seleccionó `salesforce/codet5-base` frente a `Qwen/TinyLlama` por su arquitectura encoder-decoder, ideal para traducción de lenguaje natural a código.
* **Pre-entrenamiento:** Incluye datasets masivos de código (GitHub), permitiendo entender tuberías (pipes), awk, sed y regex nativamente.
* **Eficiencia:** Con 1.5B parámetros, es el tamaño límite perfecto para ser entrenado en la VRAM limitada (15GB) de una Tesla T4 y ejecutado posteriormente en portátiles.

## 3. Ingeniería de Datos (Dataset)

La estrategia de datos se centró en la limpieza agresiva para eliminar el formato "chat" y forzar un formato "instrucción".

### 3.1. Fuentes y Limpieza
Se combinaron datasets públicos (NL2Bash, Commandlinefu) con un archivo privado `gold_commands.jsonl`.
Se desarrolló un script de pre-procesamiento con **Expresiones Regulares (Regex)** para sanear líneas corruptas (e.g., `<br>`) que rompían el pipeline de entrenamiento estándar.

### 3.2. Template de Entrenamiento
Se estandarizó el input para condicionar al modelo a responder siempre con bloques de código Markdown:

```text
User: {instrucción}
Assistant: ```bash
{comando}
```

## 4. Metodología de Entrenamiento (Fine-Tuning)

### 4.1. Aceleración con Unsloth
Se utilizó la librería **Unsloth**, que optimiza la retropropagación y reduce el consumo de memoria en un 60% comparado con HuggingFace nativo. Esto permitió:
* Usar un `batch_size` mayor.
* Acelerar el entrenamiento en un 2x.
* Exportar directamente a GGUF sin pasos intermedios complejos.

### 4.2. Hiperparámetros Críticos
* **Cuantización:** 4-bit (Load in 4bit).
* **LoRA Rank (r):** 16.
* **Target Modules:** `q_proj`, `k_proj`, `v_proj`, `o_proj`, `gate_proj`, `up_proj`, `down_proj` (Todos los módulos lineales para máxima adaptación).
* **Epochs:** 1 (Para preservar la generalización del modelo base).
* **Learning Rate:** 2e-4.

## 5. Despliegue e Inferencia

### 5.1. Exportación GGUF
Gracias a Unsloth, el modelo se exportó directamente a formato GGUF (`q4_k_m`) desde el notebook de Colab, listo para su consumo en local.

### 5.2. Modelfile (Jaula de Comportamiento)
Para producción en **Ollama**, se diseñó un `Modelfile` que elimina la temperatura (creatividad = 0) y pre-escribe el inicio de la respuesta con ` ```bash ` para forzar al modelo a completar el código.
