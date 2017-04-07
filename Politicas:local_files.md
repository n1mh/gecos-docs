# Archivos locales #

## Descripción ##

La política **Archivos locales** realiza operaciones con ficheros en local, desde el propio equipo. Las operaciones implementadas son la copia y el borrado.

Los ficheros se copian desde una URL y se puede configurar algunos aspectos de la operación, como la elección de los permisos y propietario a aplicar. Si la operación es el borrado de ficheros se puede escoger si hacer una copia de seguridad antes.

Políticas relacionadas: [folder_sync](https://github.com/gecos-team/gecos-doc/wiki/Politicasfolder_sync).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-localfiles.png" width="600" alt="px">

### Elementos del formulario ###

Se pueden especificar tantos ficheros como se desee en ambas secciones.

**Copiar fichero**

| Parámetro | Descripción | Valor por defecto(1) |
| ----------| ------------| ---------------------|
| **Usuario** | Usuario al que pertenecerá el fichero. | `root`(2) |
| **Grupo** | Grupo al que pertenecerá el fichero. | El grupo principal del usuario |
| **URL del archivo** | Dirección donde se encuentra el fichero. | Parámetro obligatorio |
| **Ruta del archivo** | Ruta de destino donde copiar el fichero. | Parámetro obligatorio(3) |
| **Permisos** | Permisos del fichero. | valor octal `755` (`rwxr-xr-x`) |
| **Sobrescribir** | Establece si se reescribe en caso de que ya exista. | No sobreescribir |

(1) Si se omite el valor de alguno de los parámetros opcionales, se tomará el indicado en esta columna.
(2) La omisión de un usuario por defecto puede ser arriesgada puesto que el usuario por defecto es `root` y puede acarrear problemas de diversa índole.
(3) Si se indica como destino un directorio, el nombre del fichero destino será el mismo que el del fichero origen.

**Borrar fichero**.

| Parámetro | Descripción |
| --------- | ----------- |
| **¿Crear copia de seguridad?** | Crea una copia de seguridad del fichero en el directorio `/var/chef/backup`. |
| **Archivo** | Fichero a borrar. |

## Implicaciones de retirar la política ##

Se deja de vigilar que el fichero indicado en la política ha sido copiado o borrado según el caso.

## Reversibilidad ##

La política no almacena información sobre los ficheros copiados o borrados y, por tanto, no es reversible aunque se pueda tener instalada sin especificar fichero alguno.

## Ejemplo ##

Con el objetivo de mantener un fondo de pantalla unificado entre todos los ordenadores de una unidad organizativa, se instala la política **Archivos locales** y se configura para que copie un fichero, el fondo de pantalla, con la siguiente información:

* Usuario: `root`
* Grupo: `root`
* URL del archivo: `https://2016.penguicon.org/wp-content/uploads/2015/12/Tux.jpg`
* Ruta del archivo: `/usr/share/backgrounds`
* Permisos: `644`
* Sobreescribir: no marcar

De esta forma el fichero con el fondo estará disponible en la ruta `/usr/share/backgrounds/Tux.jpg` y podrá ser referenciado con la política **Fondo de escritorio**.
