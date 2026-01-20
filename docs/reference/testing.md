# Pruebas de Validación y Rendimiento

**Referencia sobre la batería de pruebas realizadas.**

## 1. Pruebas Unitarias

### RAG (Retrieval-Augmented Generation)
* **Objetivo:** Verificar ingesta y recuperación.
* **Resultado:** Recuperación correcta (< 200ms) en base local.

### MQTT Bus
* **Objetivo:** Comunicación asíncrona.
* **Resultado:** Latencia < 10ms. Persistencia de mensajes correcta.

## 2. Pruebas de Integración

### End-to-End Voz
* **Flujo:** Audio -> STT -> NLU -> Lógica -> TTS.
* **Resultado:** Tiempo total lógico ~0.5s.

### Interrupción (Barge-in)
* **Escenario:** Usuario interrumpe al TTS.
* **Resultado:** Audio detenido en < 300ms.

## 3. Rendimiento y Estrés (RPi 4)

### Consumo
* **Idle:** CPU 2-5%, RAM 450MB. (Objetivo Cumplido)
* **Thinking (Gemma-2B):** CPU 380% (Saturación), RAM 1.8GB. Requiere disipación activa.

### Latencia Percibida
1. **VAD:** 500ms
2. **STT:** 800ms - 1.5s
3. **LLM:** 500ms
4. **TTS:** 200ms
* **Total:** ~2.5 - 3.0s

## 4. Conclusiones
El sistema es estable gracias a `gc.collect()`. El cuello de botella principal es la CPU en inferencia. Se recomienda RPi 5 para mejorar latencia.
