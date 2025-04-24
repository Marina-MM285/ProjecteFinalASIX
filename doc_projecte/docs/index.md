# Projecte Final: Monitorización de Red y Servicios con Pandora FMS en GNS3

## Estructura del Escenario en GNS3

### Dispositivos y Red
**NAT**

**Ubuntu Server (Servidor DHCP)**:
  
  - Pandora FMS


**Routers**
  
  - Cisco
  - Asignar direcciones IP:
    - **Xarxa 1**: `192.168.10.0/24`.
  - Mikrotik
  - Asignar direcciones IP:
    - **Xarxa 2**: `172.16.10.0/24`.


**Router Cisco**:
  
  - Dispositivos conectados:
    - VPC (IP asignada por DHCP).
    - Ubuntu Desktop (IP reservada: `192.168.10.50`, servidor web).
    - Windows 10 (IP reservada: `192.168.10.60`, servicio de archivos).


**Router Mikrotik**:
  
  - Dispositivos conectados:
    - VPC (IP asignada por DHCP).
    - Ubuntu Desktop (IP reservada: `172.16.10.50`, servidor MySQL).
    - Windows 10 (IP reservada: `172.16.10.60`, servicio de archivos).

*FOTOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO*

-------------------------------------------------------------------------------------












