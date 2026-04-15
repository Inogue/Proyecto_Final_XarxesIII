# Edificio MB – Sede Central

| Ubicación | Dispositivo / Función | VLAN | IP asignada | Observaciones |
|---|---|---:|---|---|
| MB | Firewall principal – Gestión | 10 | 192.168.10.1 | Gateway de la VLAN de gestión |
| MB | Gateway Jefes | 11 | 192.168.11.1 | Puerta de enlace VLAN 11 |
| MB | Gateway Oficinas | 12 | 192.168.12.1 | Puerta de enlace VLAN 12 |
| MB | Gateway Calidad | 13 | 192.168.13.1 | Puerta de enlace VLAN 13 |
| MB | Gateway IoT Sede | 14 | 192.168.14.1 | Puerta de enlace VLAN 14 |
| MB | Servidor DHCP/DNS interno | 10 | 192.168.10.10 | Servicio interno |
| MB | Servidor RADIUS | 10 | 192.168.10.11 | Autenticación Wi-Fi 802.1X |
| MB | Gateway DMZ | 99 | 192.168.99.1 | Interfaz DMZ del firewall |
| MB | Servidor Web público | 99 | 192.168.99.10 | Publicación externa |

# Edificio Casillas – Ventas Físicas

| Ubicación | Dispositivo / Función | VLAN | IP asignada | Observaciones |
|---|---|---:|---|---|
| Casillas | Switch principal de gestión | 10 | 192.168.10.2 | Correcto si VLAN 10 está extendida |
| Casillas | WLC / Controladora Wi-Fi | 10 | 192.168.10.5 | Corregida para gestión centralizada |
| Casillas | Gateway Comerciales / PDAs | 20 | 192.168.20.1 | Gateway de usuarios comerciales |
| Casillas | Gateway TPVs | 21 | 192.168.21.1 | Gateway de terminales de venta |

# Fábrica – Conectada por SD-WAN

| Ubicación | Dispositivo / Función | VLAN | IP asignada | Observaciones |
|---|---|---:|---|---|
| Fábrica | Router SD-WAN – LAN Gateway | 100 | 172.16.10.1 | Gateway principal de fábrica |
| Fábrica | Gateway Cámaras / IoT | 101 | 172.16.11.1 | Segmento IoT industrial |
| Fábrica | Servidor de control industrial | 101 | 172.16.11.10 | PLC / control cámaras |

# VPN – Acceso remoto

| Ubicación | Función | Rango IP | Observaciones |
|---|---|---|---|
| VPN | Pool Camiones | 10.10.1.10 – 10.10.1.110 | Acceso remoto para vehículos |
| VPN | Pool Comerciales externos | 10.10.2.10 – 10.10.2.85 | Acceso remoto para personal |
