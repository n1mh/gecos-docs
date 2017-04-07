# Administración de red #

## Descripción ##

La política **Administración de red** permite configurar las conexiones de red del equipo, ya sea cableada, inalámbrica, GSM, VPN, así como también los parámetros de proxy.

Se pueden establecer tantas conexiones como sean necesarias aunque únicamente se puede aplicar a nivel de puesto.

Políticas relacionadas: [cert](https://github.com/gecos-team/gecos-doc/wiki/Politicascert) y [web_browser](https://github.com/gecos-team/gecos-doc/wiki/Politicasweb_browser).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc-network.png" width="600" alt="px">

### Elementos del formulario ###

**General**

| Parámetro | Descripción |
| --------- | ----------- |
| **Nombre de la red** | Nombre que asignamos a la configuración de red actual. |
| **Tipo de conexión** | El tipo de conexión disponible puede ser cableada (`wired`) o inalámbrica (`wireless`). |
| **Dirección MAC** | La configuración se asigna a la interfaz con la dirección MAC que se suministra en este campo. |
| **DHCP** | Si se activa esta opción la configuración de red de la interfaz se le dará desde un servidor DHCP. En caso contrario se debe configurar el apartado **Dirección IP** con toda la información correspodiente. |

**Propiedades desactivadas de DHCP**

| Parámetro | Descripción |
| --------- | ----------- |
| **DNS** | Dirección del servidor DNS. Para evitar fallos se recomienda utilizar al menos dos servidores DNS. |
| **Máscara de red** | Proporciona la mascara de red al equipo. |
| **Dirección IP** | Proporciona la dirección IP al equipo. |
| **Puerta de enlace** | Proporciona la puerta de enlace al equipo. |

**Configuración Wireless**

| Parámetro | Descripción |
| --------- | ----------- |
| **ESSID** | Nombre de la red inalámbrica a la que se conectará el equipo. |

**Configuración de Seguridad**

| Parámetro | Descripción |
| --------- | ----------- |
| **Tipo de seguridad** | Puede elegir entre distintos tipos de seguridad como WEP, WPA y más. |
| **Tipo de autenticación** | Puede elegir entre OpenSystem y SharedKey. |
| **Contraseña** | Contraseña para la configuración de seguridad de los tipos WEP o WPA. |
| **Nombre de usuario** | Usuario a emplear en el modo LEAP. |
| **Contraseña** | Contraseña a utilizar en el modo LEAP. |

## Implicaciones de retirar la política ##

Se deja de vigilar que las conexiones de red estén configuradas tal y como se indica en la política.

## Reversibilidad ##

Esta política es reversible puesto que se permite la eliminación de toda la información suministrada para devolver al equipo al estado inicial.

## Ejemplo ##

Se quiere configurar varios ordenadores para que se conecten a una red inalámbrica concreta que está activa y configurada. En los equipos se instala la política **Administración de red** y se configura con los siguientes datos:

* General
	* Nombre de la red: Conexion Wifi Principal
	* Tipo de conexión: `wireless`
	* Dirección MAC: aa:bb:cc:dd:ee:ff
	* DHCP: activado
* Configuración Wireless
	* ESSID: principal01
* Configuración de seguridad
	* Tipo de seguridad: WPA_PSK
	* Tipo de autenticación: no modificar
	* Contraseña: Ultr4S3cur3P4ssW0rd!
	* Nombre de usuario: no modificar
	* Contraseña: no modificar

Al salvar y aplicar a los equipos, éstos podrán acceder a la red inalámbrica `principal01` tras el reinicio de la máquina puesto que hay que reiniciar el servicio de red.
