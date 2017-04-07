# Fondo de escritorio #

## Descripción ##

La política **Fondo de escritorio** permite establecer un fondo de pantalla concreto en los ordenadores GecOS.

Políticas relacionadas: [screensaver](https://github.com/gecos-team/gecos-doc/wiki/Politicasscreensaver) y [local_files](https://github.com/gecos-team/gecos-doc/wiki/politicasLocalFile).
## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-background.png" width="600" alt="px">

### Elementos del formulario ###

|  Parámetro     | Descripción |
| -------------- | ------------|
|  **Imagen**    | Ruta absoluta del equipo que apunte a la imagen a utilizar de fondo de pantalla. |

## Implicaciones de retirar la política ##

Al retirar la política se deja de controlar el fondo de escritorio, aunque no se cambia la imagen volviendo a colocar la que había antes de aplicarla.

## Reversibilidad ##

Esta política no es reversible puesto que no guarda información alguna de la imagen anterior y tampoco permite que se salven los cambios cuando el campo del formulario está en blanco.

## Ejemplo ##

Si la imagen deseada ya se encuentra en el equipo, introduzca la ruta absoluta en el cuadro **Imagen** de la política **Fondo de escritorio** y pulse el botón **Guardar**. Al aceptar los cambios, verá que el cambio se aplica a los usuarios sin privilegios del sistema. Inicie sesión con uno de ellos y espere a que se actualice para comprobar que el fondo de escritorio ha cambiado.

En un entorno de producción el fondo de escritorio estaría empaquetado y se referenciaría desde esta política.