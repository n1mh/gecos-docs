# Lanzador de scripts #

## Descripción ##

La política **Lanzador de scripts** permite añadir scripts al sistema que serán ejecutados durante el arranque o el apagado del mismo. Los scripts deben estar en el ordenador, ser ejecutables y accesibles (con los permisos adecuados). También pueden emplearse comandos del sistema que deben estar en alguno de los directorios de ejecutables.

Esta política se puede aplicar a unidades organizativas y equipos.

Políticas relacionadas: [user_apps_autostart](https://github.com/gecos-team/gecos-doc/wiki/user_apps_autostart).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-scriptslauncher.png" width="600" alt="px">

### Elementos del formulario ###

Se pueden incluir tantos scripts como se desee.

| Parámetro | Descripción |
| --------- | ----------- |
| **Script para ejecutar al inicio** | Ruta absoluta hasta el script que se quiere lanzar durante el arranque del sistema. |
| **Script para ejecutar al apagado** | Ruta absoluta hasta el script que se quiere lanzar durante el apagado del sistema. |

## Implicaciones de retirar la política ##

Se retira el lanzamiento de los scripts indicados.

## Reversibilidad ##

No es una política reversible porque no deja el equipo en el mismo estado que tenía cuando se instaló ya que pueden quedar scripts residuales en el equipo.

## Ejemplo ##

Es necesario mantener un registro de entrada de los usuarios del sistema.

Se crea (o sube un mediante un paquete de software) un script llamado `user_reg.sh` en el directorio `/usr/local/bin` con el siguiente contenido:

~~~
#!/bin/sh

echo "`date +%Y%m%d:%H%M%S` - $USER" >> /var/log/user.log
~~~

Instale la política **Lanzador de scripts** y configure el apartado **Script para ejecutar al ejecutar al inicio** con la ruta `/usr/local/bin/user_reg.sh`. Guarde y aplique los cambios.

Una vez ejecutado el cliente Chef en el equipo, inicie sesión con un usuario y compruebe que se ha registrado la información del login en el fichero `/var/log/user.log`.
