# Salvapantallas #

## Descripción ##

La política **Salvapantallas** configura el comportamiento del protector de pantalla en el equipo. Los valores que se pueden modificar son:

* permitir o no el bloqueo de la pantalla
* tiempo de inactividad hasta el bloqueo
* oscurecer la pantalla o no
* tiempo de activación del salvapantallas

Esta política se aplica a unidades organizativas y usuarios.

Políticas relacionadas: [desktop_background](https://github.com/gecos-team/gecos-doc/wiki/Politicasdesktop_background).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-screensaver.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **Permitir bloqueo de pantalla** | Si se activa esta casilla el salvapantallas solicitará la contraseña del usuario que ha iniciado sesión para desbloquearlo. |
| **Tiempo hasta el bloqueo** | Número de segundos que transcurren desde que se activa el salvapantallas hasta que se bloquea. |
| **Oscurecer pantalla** | Si se activa esta casilla la pantalla se oscurecerá hasta apagarse a modo de salvapantallas. |
| **Retraso de inactividad** | Número de segundos que deben transcurrir de inactividad hasta que se active el salvapantallas. |

## Implicaciones de retirar la política ##

Se deja de vigilar que el salvapantallas y su configuración sean los indicados en la política.

## Reversibilidad ##

Esta política es reversible puesto que permite establecer los valores vacíos (aquellos que vienen por defecto en la misma), salvar y aplicar los cambios.

## Ejemplo ##

Se quiere configurar una política de salvapantallas común acorde al documento de seguridad en las TI vigente, para toda una unidad organizativa.

Instalar la política **Salvapantallas** en la unidad organizativa y configurarlo según el documento, con los siguientes datos:

* Permitir bloqueo de pantalla: activado
* Tiempo hasta el bloqueo: 90
* Oscurecer pantalla: activado
* Retraso de inactividad: 3

Salvar y aplicar la política para distribuir los cambios.
