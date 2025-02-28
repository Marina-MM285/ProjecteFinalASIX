
# Projecte Final: Monitorizació de Xarxa i Servicis amb Pandora FMS en GNS3

## Estructura del Escenari en GNS3

### Dispositius i Xarxa
- **NAT**: Conectat a Internet i al servidor DHCP.
- **Ubuntu Server (Servidor DHCP)**:
  - Asigna direccions IP en dos xarxes:
    - **Xarxa 1**: `192.168.10.0/24` (primer switch).
    - **Xarxa 2**: `172.16.10.0/24` (segon switch).
- **Switch 1**:
  - Dispositius conectados:
    - Firefox (IP reservada: `192.168.10.10`).
    - VPC (IP asignada per DHCP).
    - Ubuntu Desktop (IP asignada per DHCP, servidor web).
- **Switch 2**:
  - Dispositius conectados:
    - Firefox (IP reservada: `172.16.10.10`).
    - VPC (IP asignada per DHCP).
    - Ubuntu Desktop (IP asignada per DHCP, servidor MySQL).

-------------------------------------------------------------------------------------

## Configuración del Servidor DHCP (Ubuntu Server)

1. **Instalar el servidor DHCP**:
   ```bash
   sudo apt update
   sudo apt install 