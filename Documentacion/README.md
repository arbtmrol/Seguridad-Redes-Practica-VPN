# Documentación del Laboratorio VPN Site-to-Site con FortiGate

## Información del estudiante

**Nombre:** Albert Morel

**Matrícula:** 2025-0833

**Asignatura:** Seguridad de Redes

---

# Propósito

Implementar una VPN Site-to-Site entre dos dispositivos FortiGate para permitir la comunicación segura entre una red de usuarios y un servidor web ubicado en una red remota.

---

# Topología

La infraestructura implementada está compuesta por:

- 2 Firewalls FortiGate.
- 1 Router ISP.
- 2 Switches.
- 1 Equipo cliente (PC1).
- 1 Servidor Web.
- Conexión hacia Internet (Cloud).
- Túnel VPN Site-to-Site.

La imagen de la topología se encuentra en el archivo **Topologia.png** ubicado en la raíz del repositorio.

---

# Configuración realizada

Durante el laboratorio se realizaron las siguientes configuraciones:

- Configuración de interfaces.
- Asignación de direcciones IP.
- Configuración de rutas estáticas.
- Configuración del túnel VPN Site-to-Site.
- Configuración de políticas de Firewall.
- Configuración de NAT.
- Configuración de DHCP.
- Validación de la comunicación entre las redes.

---

# Validación

Se realizaron las siguientes pruebas para comprobar el correcto funcionamiento:

- Estado del túnel VPN.
- Comunicación mediante Ping.
- Prueba de Traceroute.
- Comunicación entre PC1 y el servidor remoto.

Las capturas se encuentran en la carpeta **Evidencias**.

---

# Archivos incluidos

## Evidencias

- Estado del túnel VPN.
- Ping.
- Traceroute.
- Topología.

## Running Configs

- FGT1_running-config.conf
- FGT2_running-config.conf

---

# Conclusión

La implementación permitió establecer correctamente una comunicación segura mediante una VPN Site-to-Site entre ambas redes. Las pruebas de conectividad verificaron que el túnel funciona correctamente y que el tráfico puede intercambiarse entre los extremos configurados.
