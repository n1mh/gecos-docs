# Administración de paquetes #

## Descripción ##

La política **Administración de paquetes** permite instalar o desinstalar paquetes de software en una estación, pudiendo gestionarse desde una unidad organizativa a equipos concretos. Esta política permite la gestión de los catálogo de aplicaciones accesibles desde la política [software_sources](https://github.com/gecos-team/gecos-doc/wiki/politicasSoftware).

Políticas relacionadas: [app_config](https://github.com/gecos-team/gecos-doc/wiki/politicasapp_config), [auto_updates](https://github.com/gecos-team/gecos-doc/wiki/politicasauto_updates) y [software_sources](https://github.com/gecos-team/gecos-doc/wiki/politicasSoftware).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-package.png" width="600" alt="px">

### Elementos del formulario ###

Se pueden configurar tantos paquetes como sean necesarios, en ambas listas.

| Parámetro | Descripción |
| --------- | ----------- |
| **Lista de paquetes para instalar** | Lista de los nombres de paquetes a instalar. Cada paquete irá en un campo diferente. |
| **Lista de paquetes para eliminar** | Lista de los nombres de paquetes a desinstalar. Cada paquete irá en un campo diferente. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los paquetes indicados en la política estén instalados o desinstalados.

## Reversibilidad ##

Esta política no es reversible ya que no almacena el estado del equipo antes de instalarla y, consecuentemente, no hay forma de volver a ese punto una vez utilizada para modificar los paquetes de la máquina.

## Ejemplo ##

Se necesita un determinado software en todos los equipos de la unidad organizativa.

Se instala en la política **Administración de paquetes** en el nivel más alto posible, en la unidad organizativa. En la sección **Administración** se configura el repositorio donde están los paquetes del software y, a continuación, se busca el paquete en la **Lista de paquetes para instalar** y se selecciona.

Se guardan los cambios y se aplican los cambios. El nuevo software se desplegará en los todos los equipos de la unidad organizativa y estará disponible en poco tiempo.
