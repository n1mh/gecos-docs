# Usuarios #

## Descripción ##

La política **Usuarios** gestiona aquellos usuarios locales a los equipos sobre los que actúa y que no están gestionados con sistemas externos de directorios como LDAP o Active Directory.

Las operaciones que permite realizar sobre los usuarios locales del puesto son:
* creación
* modificación
* eliminación

Se pueden realizar tantas acciones sobre usuarios como se desee en una operación de la política.


En caso de que se borre la política y se vuelva a instalar para volver a gestionar usuarios, debe suministrarse toda la información relativa al usuario de nuevo, incluso si es para borrarlo. En caso de que algún campo esté vacío, la operación no se llevará a cabo.

Aunque la contraseña del usuario se muestra en texto plano, legible, se codifica a la hora de gestionar el usuario. Pero puesto que se trata de una política que permite al administrador ver la contraseña de un usuario local, no debe emplearse más que con usuarios de bajos requerimientos de seguridad.

Políticas relacionadas: [local_admin_users](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_admin_users) y [local_groups](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_groups).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-localusers.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **Acción** | La acción a realizar sobre el usuario: crear, modificar o eliminar. |
| **Usuario** | El nombre del nuevo usuario. |
| **Contraseña** | La contraseña que tendrá el usuario. Se muestra en texto plano y legible. |
| **Nombre Completo** | El nombre completo que tendrá el usuario. |
| **Grupos** | Los grupos a los que debe pertenecer. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los usuarios indicados en la política estén creados, modificados o eliminados, según el caso.

## Reversibilidad ##

Esta políitica no es reversible puesto que no guarda el estado previo de la máquina y no puede volver a el. Además, al eliminar la política no se tiene en cuenta a los usuarios ya creados y se dejan en el sistema.

## Ejemplo ##

Es necesario crear un usuario que esté activo durante una jornada de trabajo para permitir la conexión al equipo de un usuario temporal. Al finalizar dicha jornada se eliminará del puesto.

Se instala la política **Usuarios** en el puesto concreto y se genera un nuevo usuario con los siguientes datos:

* Acción: create
* Usuario: tempuser
* Contraseña: TempP4ssw0rd!
* Nombre Completo: Usuario temporal
* Grupo: users

Al aplicar los cambios en el puesto se podrá iniciar sesión con el nuevo usuario. Una vez expirado el periodo de uso se cambiará la acción a **delete** y se aplicará para eliminar el usuario.
