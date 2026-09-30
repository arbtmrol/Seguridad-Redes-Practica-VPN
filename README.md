# Laboratorio VPN Site-to-Site con FortiGate

## Datos del estudiante

**Nombre:** Albert Morel  
**Matrícula:** 2025-0833  
**Asignatura:** Seguridad de Redes  

## Propósito del laboratorio

El propósito de este laboratorio es implementar y comprobar una comunicación segura entre una red de usuarios y un servidor web utilizando un enlace VPN Site-to-Site entre dos dispositivos FortiGate.

La práctica permite comprobar que el usuario puede comunicarse con el servidor web cuando el túnel VPN se encuentra activo y que la comunicación deja de funcionar cuando el enlace VPN se encuentra deshabilitado.

## Objetivos

- Configurar dos dispositivos FortiGate mediante la interfaz gráfica.
- Configurar las interfaces de red.
- Configurar las direcciones IP correspondientes.
- Configurar NAT.
- Configurar una VPN Site-to-Site entre los dos FortiGate.
- Configurar una red de usuarios mediante VLAN 10.
- Configurar DHCP para los usuarios.
- Configurar un servidor web mediante HTTPS.
- Comprobar la comunicación entre el usuario y el servidor.
- Comprobar que la comunicación depende del enlace VPN.
- Realizar un traceroute desde el usuario hacia el servidor.

## Topología

La infraestructura está compuesta por:

- 2 FortiGate.
- 1 router ISP.
- 2 switches.
- 1 usuario.
- 1 servidor web.
- 1 conexión hacia Cloud/Internet.
- 1 túnel VPN Site-to-Site entre los FortiGate.

## Demostración

En el video demostrativo se mostrará:

1. La fecha y hora.
2. La topología implementada.
3. El estado del túnel VPN.
4. La comunicación del usuario con el servidor web mediante HTTPS.
5. El funcionamiento del traceroute.
6. La desactivación del enlace VPN.
7. La comprobación de que la comunicación deja de funcionar.
8. La activación nuevamente del enlace VPN y la recuperación de la comunicación.

## Evidencias

Las imágenes, configuraciones y evidencias de las pruebas realizadas se encuentran organizadas dentro de las carpetas correspondientes de este repositorio.
