# WatermelonD Nano Roadmap

Este documento describe la hoja de ruta para la evolución del proyecto WatermelonD Nano.

---

## Logros Completados (Fase 1 & 2 - Cimientos y Expansión)

Hitos alcanzados en la arquitectura base, optimización y nuevas capacidades.

- [X] **Refactorización Core**: Modularización de `WatermelonD.py`, `voice_manager.py`, `intent_manager.py`.
- [X] **Integración IA Local**: Implementación de **Gemma 2B / MANGO T5** optimizados para CPU.
- [X] **Memoria RAG**: Sistema de recuperación de información (Hechos/Recuerdos) usando SQLite FTS5.
- [X] **Interfaz Visual**: Dashboard "Face" con monitor de sistema (CPU/RAM/Temp) en tiempo real.
- [X] **Gestión Web**: Panel de administración con Terminal, Logs, WiFi y Configuración.
- [X] **Personalidad TIO**: Ajuste de prompts para respuestas breves, sarcásticas y en jerga española.
- [X] **Comandos de Voz de Sistema**: Reiniciar servicios, actualizar sistema, buscar archivos.
- [X] **Aprendizaje Activo**: TIO pregunta si no sabe algo y guarda la respuesta. Web de gestión de conocimiento.
- [X] **Análisis de Sentimiento**: Detección de emociones (Enfadado/Feliz) y ajuste de personalidad.
- [X] **Memoria a Largo Plazo**: Generación automática de resúmenes diarios con IA.
- [X] **Network Bros (MNB)**: Agentes satélite para Raspberry Pi Zero y ESP32 (MQTT).
- [X] **Control Multimedia**: Soporte para Chromecast (`pychromecast`) y VLC.
- [X] **Laboratorio de Fine-Tuning**: Scripts para entrenar adaptadores LoRA.

---

## Fase 3: Integración y Automatización (Corto Plazo)

Consolidar las nuevas funciones y conectarlas entre sí.

- [X] **Integración MQTT en WatermelonD**:
 - Crear un `MQTTManager` en TIO para recibir datos de los agentes "Network Bros".
 - Reaccionar a eventos (ej: "Alerta de temperatura en el salón").
- [ ] **Integración Home Assistant**:
 - Conectar TIO con Home Assistant vía API/WebSocket.
 - Controlar luces y enchufes inteligentes por voz ("Enciende la luz del salón").
- [X] **Automatización de Tareas (Cron)**:
 - Interfaz web para programar tareas recurrentes (ej. "Reinicia el router cada martes a las 3AM").
- [X] **Explorador de Archivos Web**:
 - Interfaz gráfica para navegar por `/`, ver logs y editar archivos de configuración.

---

## Fase 4: Refinamiento Cognitivo (Medio Plazo)

Mejorar la "calidad de vida" de la IA y su interacción.

- [X] **MANGO T5 V2 (NL2Bash)**:
 - Integración de modelo T5 especializado para traducir lenguaje natural a comandos Bash complejos y seguros.
- [ ] **Feedback Sonoro**:
 - Sonidos de UI (beep, confirmación) para acciones sin voz.
- [X] **Visión Artificial Mejorada**:
 - Detección de presencia mediante webcam.
- [X] **Reconocimiento Robusto (Fuzzy)**:
 - Implementación de `rapidfuzz` para detectar intenciones con tolerancia a fallos.
- [X] **Voz Neuronal (Piper)**:
 - Integración nativa de Piper TTS con modelo `es_ES-davefx-medium`.

---

## Fase 5: Futuro y Experimentación

Tecnologías avanzadas para cuando el hardware lo permita.

- [ ] **Clonación de Voz Real-Time**:
 - Usar modelos tipo Coqui TTS/XTTS para darle una voz única y clonada dinámicamente.
- [ ] **Interfaz Holográfica**:
 - Proyección o uso de pantallas transparentes para el "Face".
- [ ] **LLM Upgrade (Llama 3 8B)**:
 - Migrar a modelos de 8B parámetros cuantizados (requiere upgrade de hardware/RAM > 16GB).
- [X] **Estructura de Embeddings Vectoriales (ChromaDB)**:
 - Implementada base para búsqueda semántica.
 - Integrado en ChatManager.
 - Interfaz web para re-entrenamiento (`/knowledge`).
- [ ] **Multimodalidad (LLaVA / BakLLaVA)**:
 - Integración de modelos de visión-lenguaje para "ver" y describir imágenes en tiempo real.

---

## Fase 6: Ecosistema SysAdmin (Implementado)

Herramientas de gestión y control.

- [X] **Gestor Docker**:
 - Skill de voz con MANGO T5 ("Reinicia el contenedor de Pi-hole").
 - Panel web `/docker` para gestión y visualización de logs.
- [X] **Monitor de Red & Speedtest**:
 - Comandos de velocidad implementados.
 - API de red funcional.
- [X] **Notificaciones Remotas (Telegram/Discord)**:
 - Bot para alertas al móvil: "Tío, se ha ido la luz" o "Alerta de temperatura".
- [ ] **Dashboard Histórico**:
 - Gráficas de temperatura/CPU de las últimas 24h (RRDTool/Prometheus).

---

## Fase 7: Evolución Cognitiva y Autonomía (Propuesta Nueva)

El siguiente salto evolutivo hacia una IA Agente autónoma.

- [ ] **Biometría de Voz (Speaker ID)**:
 - Integrar `pyannote.audio` o similar para distinguir *quién* habla.
 - Permisos por usuario ("Solo Juan puede apagar el servidor").
- [ ] **Orquestación Multi-Agente (Swarm)**:
 - Descomponer TIO en micro-agentes especializados:
 - *Agent-Security*: Monitoriza logs de `auth.log` en segundo plano.
 - *Agent-Media*: Gestiona descargas y biblioteca multimedia.
 - *Agent-Home*: Gestiona la domótica.
- [X] **Self-Healing (Autocuración)**:
 - Detección proactiva de fallos (ej: "nginx caído") y reinicio automático sin intervención humana.
- [X] **Base de Conocimiento Offline (Small LM)**:
 - Integrar un modelo pequeño (Phi-2 / TinyLlama) dedicado exclusivamente a conocimiento enciclopédico local (Wiki reducida) para no depender de internet.

---

## Hitos Recientes (v3.0.0 Stable)

### Web Interface V3 & Core V4
- [X] **Core Nativo Optimizado (V4)**:
 - Watchdog de hilos para autocuración interna.
 - Optimización de PyTorch para CPUs i3 (gestión de hilos).
- [X] **Web UI V3 (Cosmic Polish)**:
 - Dashboard con Drag-and-Drop persistente.
 - Sistema de notificaciones unificado (Toast + Desktop).
 - Monitor de conexión a pantalla completa.
 - Sección de Actualizaciones y "Acerca de".
