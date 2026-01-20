# Documentación de Seguridad

**Defensa en Profundidad**: Protección desde la web hasta el kernel.

## 1. Seguridad Web (Admin Panel)

### Autenticación
* **Hashing**: PBKDF2/SHA256. Nunca texto plano.
* **Helper**: `password_helper.py` para gestión segura CLI.

### Encriptación HTTPS
* **SSL/TLS**: Certificados autofirmados generados al instalar.
* **HSTS**: Forzado en cabeceras.

### Protección CSRF
* **Token Global**: Inyectado en todas las plantillas y peticiones AJAX.

### Rate Limiting
* **Login**: Bloqueo temporal tras 5 intentos fallidos.

## 2. Seguridad del Sistema Operativo

### Firewall (UFW)
* **Política**: Deny Incoming, Allow Outgoing.
* **Allow**: SSH (22), Web (5000), MQTT (1883).

### Fail2Ban
* **Monitor**: `/var/log/auth.log`
* **Acción**: Ban de 1 hora tras 3 fallos SSH.

### Permisos de Archivos
* **Config/DB/Certs**: `chmod 600`. Solo legible por el usuario del servicio.

## 3. Herramientas Incluidas
* **`password_helper.py`**: Gestión de claves hash.
* **`secure_system.sh`**: Script de hardening "One-Click" (UFW, Fail2Ban, Permisos).

## 4. Mantenimiento
* **Rotación de Certificados**: Regenerar `neo.crt`/`neo.key` periódicamente.
* **Auditoría**: Revisar logs de Fail2Ban regularmente.
