# Manual de Administración

**Gestion del Servicio, Monitorización y Mantenimiento.**

## 1. Gestión del Servicio (Systemd)
El servicio corre como usuario (`neo.service`).
* **Start:** `systemctl --user start neo.service`
* **Stop:** `systemctl --user stop neo.service`
* **Logs en vivo:** `journalctl --user -u neo.service -f`

## 2. Gestión de Redes
* **Network Bros:** Agentes detectados automáticamente vía MQTT.
* **Seguridad:** Reglas `Guard` bloquean IPs sospechosas.

## 3. SSH y Acceso Remoto
* **Gestión de Servidores:** Añadir/Quitar servidores SSH para control por voz.
* **Seguridad:** Usar `ssh-agent`.

## 4. Gestión de Contenedores (Docker)
Panel web en `/docker`.
* **Control:** Start/Stop/Restart contenedores.
* **Logs:** Vista en tiempo real.

## 5. Actualizaciones
* **Web:** Botón "Actualizar NEOPapaya" en Ajustes -> Acciones.
* **Terminal:** `git pull` && `pip install -r requirements.txt`.
