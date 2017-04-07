# Administradores locales #

## Descripción ##

La política **Administradores locales** concede o revoca **privilegios de administrador** a los usuarios indicados en el formulario.

Se puede aplicar a nivel de unidad organizativa o de equipo y, forzasamente, debe aplicarse sobre usuarios existentes en el sistema, tanto para asignar como para revocar privilegios.

Se introducirá un usuario por cuadro del formulario en ambas secciones.

Políticas relacionadas: [local_groups](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_groups) y [local_users](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_users).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/local_admin_users.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro    | Descripción |
| ------------ | ----------- |
| **Usuarios** | Nombres de usuarios a los que asignarles permisos de administrador. |
| **Usuarios a eliminar** | Nombres de de usuarios a los que retirar permisos de administrador. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los usuarios indicados tengan privilegios de administrador. Para eliminar los permisos de administración debe hacerse explícitamente usando la segunda lista, "Usuarios a eliminar".

## Reversibilidad ##

Esta política no es reversible puesto que, aunque permite vaciar ambas listas del formulario, los usuarios no se modifican en el sistema. Para lograr un borrado completo de privilegios hay que utilizar la lista de revocación de privilegios explícitamente.

## Ejemplo ##

Es necesario que el usuario del sistema **manuel.cobo** pueda instalar paquetes en aquellos ordenadores que utiliza. A tal efecto se le instala  la política **Administradores locales** y se añade su nombre al formulario, en la parte de concesión de permisos.

Tras hacer efectivo el cambio el usuario debe reiniciar la sesión en caso de que estuviese conectado. Tras ese reinicio de sesión, podrá gestionar paquetes utilizando el programa `synaptic`.
