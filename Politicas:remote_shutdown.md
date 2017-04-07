# Apagado remoto #

## Descripción ##

La política **Apagado remoto** apaga o reinicia remotamente el equipo sobre el que actúa. La acción seleccionada se producirá cinco minutos después de la sincronización del puesto con el Centro de Control GecOS, es decir, después de la ejecución del cliente Chef (`chef-client`).

Para volver a utilizar la política, debe volver a aplicarse de nuevo, eliminándola y volvíendola a instalar.

En caso de que la política no se elimine, se programará la misma acción (apagado o reinicio) a un año vista, en la misma fecha que se efectúo la última.

Esta política se puede aplicar a equipos y a unidades organizativas.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-remote-shutdown.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **Tipo de apagado** | Establece la opción que permite el apagado o el reinicio remoto del equipo. |

## Implicaciones de retirar la política ##

Se elimina el apagado o reinicio temporizado del equipo.

## Reversibilidad ##

Esta política es reversible puesto que permite desactivar los dos estados seleccionando una opción vacía.

## Ejemplo ##

Se necesita que todos los ordenadores de un aula estén apagados completamente al final de la jornada.

Se instala la política **Apagado remoto** en la unidad organizativa que contiene el aula y, al finalizar la jornada, se activa para todos los ordenadores con el parámetro `halt`. Se guardan y aplican los cambios. Cinco minutos después los ordenadores comenzarán a apagarse.
