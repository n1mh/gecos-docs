# Grupos locales #

## Descripción ##

La política **Grupos locales** permite realizar operaciones con los grupos locales de un equipo. Las operaciones permitidas son añadir y eliminar usuarios del grupo seleccionado.

Hay que destacar que esta política no crea a los usuarios que gestiona y que estos ya deben existir de antemano o sino la política fallará. El grupo, por el contrario, puede crearse en caso de que no exista.

Si quiere convertir a un usuario en administrador, utilice la política [local_admin_users](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_admin_users).

Políticas relacionadas: [local_admin_users](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_admin_users) y [local_users](https://github.com/gecos-team/gecos-doc/wiki/politicasUsuarios).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-groups.png" width="600" alt="px">

### Elementos del formulario ###

Se pueden añadir tantos usuarios a un grupo como se desee.

| Parámetro | Descripción |
| --------- | ----------- |
| **Usuarios** | Lista de usuarios que se quiere que pertenezcan al grupo. |
| **Grupo** | Nombre del grupo. |
| **Eliminar usuarios** | Marcar para eliminar los usuarios especificados del grupo. |
| **Crear grupo** | Crear el grupo en caso de que no exista y añadir los usuarios. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los usuarios indicados formen parte del grupo en cuestión.

## Reversibilidad ##

Esta política no es reversible ya que no controla el estado inicial para restaurarlo al eliminarla y tampoco tiene en cuenta que puede dejar grupos o usuarios instalados en el sistema después de borrar la política.

## Ejemplo ##

Se desea añadir al usuario `fgarcia` al grupo `sambashare` para que pueda compartir directorios personales bajo el protocolo CIFS. Para ello se instala la política **Grupos locales** y se configura con la siguiente información:

* Usuarios: `fgarcia`
* Grupo: `sambashare`
* Eliminar usuarios: no marcar
* Crear grupo: marcar

Al salvar y aplicar la política, el usuario debe reiniciar la sesión en caso de que la haya iniciado puesto que la pertenencia a grupos se aplica al iniciar sesión. Tras ese paso formará parte del grupo.
