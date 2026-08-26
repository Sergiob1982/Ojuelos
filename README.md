# Ojuelos — firmware OTA

Binarios de firmware para el sistema de puerta comunitaria **RESIDENCIAL OJUELOS**
(emisores LoRa TTGO ESP32). Se publican aquí para actualización OTA:

- El emisor administrador anuncia por LoRa la versión + hash + URL de este `.bin`.
- Cada emisor descarga el `.bin` por HTTPS, verifica el hash y se autoflashea.

> El `.bin` **no contiene la clave secreta** (va en NVS de cada equipo), por eso
> puede publicarse en un repositorio público sin comprometer la seguridad.

## Archivos

| Archivo | Versión | Descripción |
|---------|---------|-------------|
| `emisor.bin` | v1.2 | Firmware del emisor (código OTA 3) — corrige el buffer de recepción LoRa (64→255 B) que impedía recibir el gatillo OTA y el registro de accesos |

URL directa (raw) para el campo de la página de actualizaciones:

```
https://raw.githubusercontent.com/Sergiob1982/Ojuelos/main/emisor.bin
```
