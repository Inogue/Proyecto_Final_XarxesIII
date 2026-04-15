# Plan de direccionamiento IP corregido

## Edificio MB – Sede Central

| Ubicación | Dispositivo / Función | VLAN | Red | IP asignada | Observaciones |
|---|---:|---|---|---|---|
| MB | Firewall principal – Gestión | 10 | 192.168.10.0/24 | 192.168.10.1 | Gateway de la VLAN de gestión |
| MB | Gateway Jefes | 11 | 192.168.11.0/24 | 192.168.11.1 | Puerta de enlace VLAN 11 |
| MB | Gateway Oficinas | 12 | 192.168.12.0/24 | 192.168.12.1 | Puerta de enlace VLAN 12 |
| MB | Gateway Calidad | 13 | 192.168.13.0/24 | 192.168.13.1 | Puerta de enlace VLAN 13 |
| MB | Gateway IoT Sede | 14 | 192.168.14.0/24 | 192.168.14.1 | IoT propio de la sede central |
| MB | Servidor DHCP/DNS interno | 10 | 192.168.10.0/24 | 192.168.10.10 | Servicio interno |
| MB | Servidor RADIUS | 10 | 192.168.10.0/24 | 192.168.10.11 | Autenticación Wi-Fi 802.1X |
| MB | Gateway IoT corporativo | 30 | 192.168.30.0/24 | 192.168.30.1 | Red IoT adicional para sensores y servicios |
| MB | Broker MQTT (Mosquitto) | 30 | 192.168.30.0/24 | 192.168.30.10 | Broker IoT |
| MB | Home Assistant | 30 | 192.168.30.0/24 | 192.168.30.11 | Plataforma de monitorización IoT |
| MB | Gateway Vídeo / Cámaras | 31 | 192.168.31.0/24 | 192.168.31.1 | Segmento separado para vídeo |
| MB | MediaMTX / NVR / Cámara IP simulada | 31 | 192.168.31.0/24 | 192.168.31.10 | Streaming RTSP / videovigilancia |
| MB | Gateway DMZ | 99 | 192.168.99.0/24 | 192.168.99.1 | Interfaz DMZ del firewall |
| MB | Servidor Web público | 99 | 192.168.99.0/24 | 192.168.99.10 | Publicación externa |

## Edificio Iker Casillas – Ventas Físicas

| Ubicación | Dispositivo / Función | VLAN | Red | IP asignada | Observaciones |
|---|---:|---|---|---|---|
| Casillas | Switch principal de gestión | 10 | 192.168.10.0/24 | 192.168.10.2 | Correcto si VLAN 10 está extendida desde MB |
| Casillas | WLC / Controladora Wi-Fi | 10 | 192.168.10.0/24 | 192.168.10.5 | Gestión centralizada |
| Casillas | AP gestionable 1 | 10 | 192.168.10.0/24 | 192.168.10.20 | Administración del AP |
| Casillas | AP gestionable 2 | 10 | 192.168.10.0/24 | 192.168.10.21 | Administración del AP |
| Casillas | Gateway Comerciales / PDAs | 20 | 192.168.20.0/24 | 192.168.20.1 | Red de comerciales y PDAs |
| Casillas | Gateway TPVs | 21 | 192.168.21.0/24 | 192.168.21.1 | Red de terminales de venta |
| Casillas | TPVs | 21 | 192.168.21.0/24 | DHCP | Equipos de cobro |
| Casillas | PDAs / Comerciales | 20 | 192.168.20.0/24 | DHCP | Dispositivos móviles comerciales |

## Fábrica – Conectada por SD-WAN

| Ubicación | Dispositivo / Función | VLAN | Red | IP asignada | Observaciones |
|---|---:|---|---|---|---|
| Fábrica | Router SD-WAN – LAN Gateway | 100 | 172.16.10.0/24 | 172.16.10.1 | Gateway principal de fábrica |
| Fábrica | Gateway IoT / Cámaras fábrica | 101 | 172.16.11.0/24 | 172.16.11.1 | Segmento industrial separado |
| Fábrica | Servidor de control industrial / PLC | 101 | 172.16.11.0/24 | 172.16.11.10 | Control industrial |
| Fábrica | Cámaras / sensores industriales | 101 | 172.16.11.0/24 | DHCP o IP fija según necesidad | Dispositivos industriales |

## VPN – Acceso remoto

| Ubicación | Función | Red / Pool IP | Observaciones |
|---|---|---|---|
| VPN | Pool Camiones | 10.10.1.10 - 10.10.1.110 | Acceso remoto para vehículos |
| VPN | Pool Comerciales externos | 10.10.2.10 - 10.10.2.85 | Acceso remoto para personal |
