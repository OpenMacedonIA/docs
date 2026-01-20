# Resolución de Problemas (Troubleshooting)

**Nivel:** Usuario / Técnico

Esta guía consolida soluciones a problemas comunes, desde audio hasta errores de IA.

---

## 1. Problemas de Audio

### El asistente no escucha o no habla
1. **Verificar dispositivos:**
   ```bash
   aplay -l  # Altavoces
   arecord -l # Micrófono
   ```
2. **Ajustar volúmenes:** Use `alsamixer` (Verificar que Mic no esté en "MM" mute).
3. **Logs:** Busque errores `PyAudio` o `ALSA` en `journalctl --user -u neo.service`.

### Reconocimiento de voz deficiente
1. **Ruido:** Hable más cerca del micrófono.
2. **Modelo:** Use un modelo Vosk más grande si el hardware lo permite.

---

## 2. Problemas de IA (LLM)

### Respuestas lentas o reinicios
1. **OOM (Out of Memory):** El kernel mata el proceso si falta RAM. Revise `dmesg`. Aumente Swap o use un modelo más pequeño (q2_k).
2. **Instrucciones Ilegales:** Si la CPU no soporta AVX, recompile `llama.cpp`.

### Alucinaciones
1. **Temperatura:** Reducir a 0.2 en `config.json`.
2. **System Prompt:** Reforzar instrucciones de "No lo sé".

---

## 3. Problemas de Red y MQTT

### No detecta la red
1. Verificar `ip a`.
2. Verificar DNS en `/etc/resolv.conf`.

### Error MQTT
1. Verificar estado: `sudo systemctl status mosquitto`.
2. Verificar logs de conexión en NeoCore.

---

## 4. Códigos de Error Internos

| Código | Significado | Acción |
| :--- | :--- | :--- |
| `E001` | Audio Device Not Found | Verificar hardware y permisos. |
| `E002` | MQTT Connection Lost | Revisar Mosquitto. |
| `E003` | LLM OOM | Aumentar RAM/Swap. |
| `W001` | High CPU Temp | Revisar ventilación. |
| `S001` | Auth Failure | Posible intrusión. |
