# Perfiles de Software disponibles #

## Descripción ##

La política **Perfiles de Software disponibles** permite instalar o desinstalar perfiles de paquetes de software que contienen agrupaciones de paquetes bajo una temática concreta. Por ejemplo, para instalar una suite ofimática completa basta con instalar el perfil **Office** en vez de todos los paquetes que contiene, de forma individual. La instalación y gestión de esta política se puede hacer a nivel de unidad organizativa o de equipo.

Puede controlar el catálogo de aplicaciones disponible con la política [software_sources](https://github.com/gecos-team/gecos-doc/wiki/politicasSoftware).

Políticas relacionadas: [app_config](https://github.com/gecos-team/gecos-doc/wiki/politicasapp_config), [auto_updates](https://github.com/gecos-team/gecos-doc/wiki/politicasReglas) y [software_sources](https://github.com/gecos-team/gecos-doc/wiki/politicasSoftware).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-package-profile.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **Lista de Perfiles de Software** | Lista de los nombres de los perfiles de software. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los perfiles de software estén instalados o desinstalados.

## Reversibilidad ##

Esta política no es reversible ya que no almacena el estado del equipo antes de instalarla y, consecuentemente, no hay forma de volver a ese punto una vez utilizados los perfiles para los paquetes de la máquina.

## Ejemplo ##

Se necesita una suite ofimática en todos los equipos de la unidad organizativa.

Se instala en la política **Perfiles de Software disponibles** en la unidad organizativa. En la sección **Administración** se configuran los perfiles de software y, a continuación, se busca el paquete en la **Lista de perfiles de software** y se selecciona **Office**.

Se guardan los cambios y se aplican los cambios. La suite de ofimática desplegará en los todos los equipos de la unidad organizativa y estará disponible en poco tiempo.
