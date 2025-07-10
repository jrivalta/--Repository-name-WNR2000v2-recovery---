# --Repository-name-WNR2000v2-recovery---
- Description: Proceso técnico detallado de recuperación del router Netgear WNR2000v2 utilizando UART, TFTP y CFE -

- # 🔧 Recuperación del Netgear WNR2000v2 – UART + TFTP + CFE

Este proyecto documenta el proceso técnico completo de recuperación de un router Netgear WNR2000v2 utilizando conexión UART, carga vía TFTP desde CFE y prueba exhaustiva de múltiples firmwares oficiales.  
Una demostración de cómo la persistencia técnica puede devolver la vida a hardware olvidado.

## 📦 Requisitos

- Router Netgear WNR2000v2
- Adaptador USB a TTL
- Cables jumper
- Laptop con TFTP habilitado
- Software terminal (recomendado: PuTTY, Tera Term, minicom)
- Firmwares descargados desde el sitio oficial de Netgear

## ⚙️ Conexión UART

- TX, RX y GND conectados directamente a la placa del router
- Configuración serial: `115200 8N1`, sin control de flujo
- Acceso al modo CFE para carga de firmware

## 📡 Flasheo vía TFTP

```bash
tftp -i 192.168.1.1 PUT firmware.img
