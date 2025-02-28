
# Proyecto Final: Monitorización de Red y Servicios con Pandora FMS en GNS3

## Estructura del Escenario en GNS3

### Dispositivos y Redes
- **NAT**: Conectado a Internet y al servidor DHCP.
- **Ubuntu Server (Servidor DHCP)**:
  - Asigna direcciones IP en dos redes:
    - **Red 1**: `192.168.10.0/24` (primer switch).
    - **Red 2**: `172.16.10.0/24` (segundo switch).
- **Switch 1**:
  - Dispositivos conectados:
    - Firefox (IP reservada: `192.168.10.10`).
    - VPC (IP asignada por DHCP).
    - Ubuntu Desktop (IP asignada por DHCP, servidor web).
- **Switch 2**:
  - Dispositivos conectados:
    - Firefox (IP reservada: `172.16.10.10`).
    - VPC (IP asignada por DHCP).
    - Ubuntu Desktop (IP asignada por DHCP, servidor MySQL).

---

## Configuración del Servidor DHCP (Ubuntu Server)

1. **Instalar el servidor DHCP**:
   ```bash
   sudo apt update
   sudo apt install isc-dhcp-server