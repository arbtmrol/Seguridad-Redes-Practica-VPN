# Laboratorio VPN Site-to-Site con FortiGate

## Datos del estudiante

**Nombre:** Albert Morel
**Matrícula:** 2025-0833
**Asignatura:** Seguridad de Redes

---

## Propósito del laboratorio

El propósito de este laboratorio es implementar y comprobar la comunicación entre dos redes utilizando una VPN Site-to-Site mediante dos dispositivos FortiGate.

La práctica permite demostrar la comunicación entre un equipo ubicado en la red de FGT-1 y un servidor ubicado en la red remota protegida por FGT-2, utilizando el túnel VPN configurado entre ambos dispositivos.

---

## Objetivos

* Configurar dos dispositivos FortiGate mediante su interfaz gráfica.
* Configurar las interfaces de red utilizadas en la topología.
* Configurar el direccionamiento IP correspondiente.
* Configurar las rutas necesarias para la comunicación entre las redes.
* Configurar una VPN Site-to-Site entre FGT-1 y FGT-2.
* Configurar las políticas necesarias para permitir la comunicación.
* Comprobar la conectividad entre el equipo de usuario y el servidor remoto.
* Realizar una prueba de `ping` entre las redes.
* Realizar un `traceroute` desde el usuario hacia el servidor.
* Verificar el estado activo del túnel VPN.

---

## Topología

La infraestructura está compuesta por:

* 2 dispositivos FortiGate.
* 1 router.
* 2 switches.
* 1 equipo PC1.
* 1 Web Server (`webterm-1`).
* 1 conexión Cloud.
* 1 túnel VPN Site-to-Site entre los FortiGate.

La topología utilizada se encuentra en:

**[Topologia.png](./Topologia.png)**

---

## Direccionamiento utilizado

### PC1

```text
IP:       192.168.10.2/25
Gateway:  192.168.10.1
```

### Web Server

```text
IP:       172.16.83.2/28
Gateway:  172.16.83.1
```

### FGT-1

```text
Port1: 200.83.33.2/30
Port2: 192.168.33.1/25
Port3: 192.168.161.101/24
```

### FGT-2

```text
Port1: 200.83.34.2/30
Port2: 172.16.83.1/28
Port3: 192.168.161.102/24
```

---

## VPN Site-to-Site

El túnel configurado en FGT-1 se identifica como:

```text
VPN_to_FGT2
```

El gateway remoto configurado corresponde a:

```text
200.83.34.2
```

Durante las pruebas, el túnel aparece activo mediante el indicador de estado de FortiGate.

---

## Pruebas realizadas

### Prueba de conectividad

Desde PC1 se realizó una prueba de conectividad hacia el Web Server:

```text
ping 172.16.83.2
```

Resultado:

```text
5 paquetes enviados
5 paquetes recibidos
0% de pérdida
```

### Traceroute

Desde PC1 se realizó:

```text
trace 172.16.83.2
```

El recorrido observado fue:

```text
192.168.10.1
200.83.34.2
172.16.83.2
```

Estas pruebas permiten comprobar la comunicación entre la red de PC1 y la red remota donde se encuentra el Web Server.

---

## Evidencias

Las evidencias de la práctica se encuentran organizadas dentro de las carpetas correspondientes del repositorio.

Entre ellas se incluyen:

* Imagen de la topología.
* Estado del túnel VPN.
* Prueba de conectividad mediante `ping`.
* Prueba de recorrido mediante `traceroute`.
* Configuraciones de los dispositivos FortiGate.

---

## Video demostrativo

**Video:** Pendiente de publicación.

El video demostrativo presentará:

1. Identificación del estudiante.
2. Fecha y hora.
3. Topología implementada.
4. Estado del túnel VPN.
5. Prueba de conectividad entre PC1 y el Web Server.
6. Prueba de `traceroute`.
7. Conclusión sobre el funcionamiento de la comunicación entre las redes.

---

## Conclusión

La práctica permitió implementar una VPN Site-to-Site entre dos dispositivos FortiGate y comprobar la comunicación entre una red de usuarios y una red remota.

Las pruebas realizadas mediante `ping` y `traceroute` demostraron que PC1 puede alcanzar el Web Server ubicado en la red remota mientras el túnel VPN se encuentra activo.

