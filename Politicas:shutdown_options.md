# Opciones de apagado #

## Descripción ##

La política **Opciones de apagado** configura las opciones de apagar, reiniciar o cerrar sesión en un equipo, para todos los usuarios del mismo.

Esta política se aplica a unidades organizativas y usuarios.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-shutdown.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **¿Desactivar apagado?** | Al activar la casilla se anula la posibilidad al usuario de poder cerrar la sesión, apagar, o reiniciar el equipo. |

## Implicaciones de retirar la política ##

Se deja de vigilar que las opciones de apagado indicadas en la política se muestran en el menú de apagado.

## Reversibilidad ##

Esta política es reversible puesto que se puede dejar el equipo en su estado inicial, que por defecto es con la opción desactivada.

## Ejemplo ##

Es necesario evitar que únicamente un usuario concreto acceda a un equipo, hasta nuevo aviso.

Se instala la política **Opciones de apagado** en el equipo y se configura para que no se permita el apagado ni el cierre de sesión. Se guarda y aplica la política.

En el equipo se inicia sesión con el usuario y se comprueba que los botones de cerrar sesión, apagar y reiniciar el equipo no se encuentran operativas aunque se muestren los iconos.
