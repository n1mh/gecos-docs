# VPN de FortiClient #

## Descripción ##

La política **VPN de FortiClient** permite configurar un puesto para que establezca una conexión VPN empleando el software de FortiClient.

Políticas relacionadas: [cert](https://github.com/gecos-team/gecos-doc/wiki/Politicascert) y [web_browser](https://github.com/gecos-team/gecos-doc/wiki/Politicasweb_browser).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-vpn.png" width="600" alt="px">

### Elementos del formulario ###

**Conexiones**

| Parámetro | Descripción |
| --------- | ----------- |
| Nombre    | Nombre que asignamos a la conexión VPN. |
| Servidor  | Servidor VPN con el que establecer conexión. |
| Puerto    | Puerto de conexión a la VPN. |

Pueden configurarse tantas conexiones diferentes como sean necesarias.

| Parámetro | Descripción |
| --------- | ----------- |
| Servidor Proxy | Dirección del servidor Proxy, en caso de utilizar uno. |
| Puerto del Proxy | Puerto del servidor Proxy. |
| Usuario del Proxy | Usuario para autenticarse en el servidor Proxy. |
| Arranque automático | Marcar si se desea una activación automatica del servidor VPN. |
| Frecuencia del keepalive | Intervalo para comprobar la conexión con el servidor. |

## Implicaciones de retirar la política ##

Se deja de vigilar que la conexión VPN este configurada tal y como se indica en la política.

## Reversibilidad ##

Aunque no se almacena el estado anterior el formulario si permite eliminar todas las configuraciones y ajustes hechos, sin eliminar la política por lo que se considera reversible.

## Ejemplo ##

La política **VPN de Forticlient** se emplea para establecer una comunicación segura

En un escenario de produción todas las comunicaciones relevantes deberían ir a través de un túnel privado y una VPN. En el caso concreto de muchas aplicaciones de la Junta de Andalucía, el uso de una conexión a través de la VPN de Forticlient se hace indispensable por lo que, para establecer conexión con estas aplicaciones es necesario instalar la política **VPN de FortiClient** y configurarla.

En el apartado de configuración se pondrán los siguientes datos:
* **Nombre**: Junta de Andalucía
* **Servidor**: https://vpn.juntadeandalucia.es
* **Puerto**: 443

De esta forma se utilizará la VPN configurada para establecer conexiones seguras.
