# Acceso directo en el escritorio #

## Descripción ##

La política **Acceso directo en el escritorio** permite situar iconos para ejecutar aplicaciones en el escritorio de los usuarios.

Esta política está disponible para unidades organizativas y usuarios.

Políticas relacionadas: [desktop_control](https://github.com/gecos-team/gecos-doc/wiki/Politicasdesktop_control) y [desktop_menu](https://github.com/gecos-team/gecos-doc/wiki/Politicasdesktop_menu).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-userlaunchers.png" width="600" alt="px">

### Elementos del formulario ###

Se pueden añadir tantos ficheros como sean necesiario.

|  Parámetro  | Descripción |
| ----------- | ------------|
| **Acceso directo** | Ruta absoluta del fichero `.desktop` (incluyendo dicha extensión) de la aplicación a colocar el escritorio. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los lanzadores indicados en la política estén en el escritorio pero no se eliminan.

## Reversibilidad ##

Esta política no es reversible puesto que no almacena el estado inicial de la máquina o los usuarios que trata y, por tanto, no puede devolverla al estado anterior a la instalación.

# Posibles errores contemplados #

Si obtenemos un error en el cual nos indica lo siguiente `2014/12/12 12:12:12: Is a directory - /home/usuario/Escritorio/` es debido a que el usuario no se ha entrado nunca en el equipo, es necesario que éste entre por primera vez en el equipo para que genere el Escritorio

## Ejemplo ##

Se quiere crear un acceso a la web del sistema Portafirmas de la Junta de Andalucía desde el escritorio de los usuarios.

Lo primero es subir a los equipos involucrados un fichero llamado `portafirmas.desktop` con el siguiente contenido:

~~~
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=Porta firmas
Comment=Junta de Andalucia
Exec=firefox %u "https://www.juntadeandalucia.es/ep-hospitalponientealmeria/portafirmas/index.htm"
Terminal=false
Type=Application
Icon=firefox
~~~

Se puede subir al directorio `/usr/share/applications` mediante un paquete de software, por ejemplo. A continuación se aplica a la unidad organizativa la política **Acceso directo en el escritorio** y se configura con la ruta `/usr/share/applications/portafirmas.desktop` y se guarda y aplica.

A los pocos minutos los equipos mostrarán el icono en el escritorio de los usuarios.
