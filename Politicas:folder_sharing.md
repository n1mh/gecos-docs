# Permisos para compartir #

## Descripción ##

La política **Permisos para compartir** establece si un usuario puede o no **compartir recursos** en red usando el protocolo CIFS de compartición de recursos de Microsoft.

Políticas relacionadas: [user_mount](https://github.com/gecos-team/gecos-doc/wiki/Politicasuser_mount)

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-sharing.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **¿Puede compartir?** | Casilla para marcar si el usuario puede compartir recursos en red. |

En caso de que el usuario al que afecta la política haya iniciado sesión, deberá volver a iniciar sesión para que surta efecto.

## Implicaciones de retirar la política ##

Se deja de vigilar que el usuario pueda o no compartir recursos en red.

## Reversibilidad ##

Esta política es reversible puesto que se puede dejar en el estado original y, posteriormente, eliminar la política para dejar el equipo en el estado inicial.

## Ejemplo ##

Seleccione un usuario o una unidad organizativa que contenga usuarios. Aplique esta política pero no marque la casilla.

Pulse **Guardar**. Encole los cambios.

Vaya al puesto de trabajo y entre con un usuario al que le esté aplicando esta política. Espere a que se actualice. Abra el administrador de archivos, seleccione una carpeta y compruebe que el usuario no puede compartirla.

Adicionalmente puede abrir un terminal de comandos y teclear **id nombredeusuario**. Se le muestran los grupos a los que pertenece el usuario y entre ellos debe estar el grupo **sambashare**
