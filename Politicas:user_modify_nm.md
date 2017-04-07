# Conceder permisos de red al usuario #

## Descripción ##

La política **Conceder permisos de red al usuario** habilita a los usuarios del equipo a modificar los parámetros de red.

Esta política está disponible para unidades organizativas y usuarios.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-user-modify.png" width="600" alt="px">

### Elementos del formulario ###

|  Parámetro  | Descripción |
| ----------- | ------------|
| **¿Permisos para modificar la red?** | Al activar la casilla le está dando permisos para modificar los parámetros de red a los usuarios. |

## Implicaciones de retirar la política ##

Los usuarios afectados por la política dejan de tener permisos para poder modificar la red.

## Reversibilidad ##

Puesto que no almacena el estado anterior a la instalación de la política y no permite volver a ese punto, esta política no es reversible.

## Ejemplo ##

Se necesita que los usuarios de un aula puedan modificar los parámetros de red.

En la unidad organizativa correspondiente se instala la política **Conceder permisos de red al usuario** y se marca la casilla para conceder el permiso.

En cuanto la política se propague los usuarios podrán modificar los parámetros de la red.
