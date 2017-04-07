# Navegador de archivos #

## Descripción ##

La política **Navegador de archivos** permite configurar el comportamiento del explorador de ficheros del sistema, `Nemo`. Las opciones a modificar son:

* número de clics para abrir archivos.
* mostrar ficheros ocultos.
* la vista de ficheros.
* mostrar el icono de búsqueda.
* el comportamiento de la papelera.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-filebrowser.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| ----------| ----------- |
| **Política de click** | Elegir el número de clics para realizar una acción. Puede ser único (un click) o doble (dos click). |
| **Mostrar archivos ocultos** | Establece si se muestran los ficheros ocultos (aquellos que comienzan con un punto) o no. |
| **Visualización de archivos** | Permite elegir la vista principal del explorador de ficheros. Las opciones son vista de iconos, vista compacta y vista de lista. |
| **Mostrar el icono de búsqueda en la barra de herramientas** | Establece si se muestra el botón para búsquedas en la interfaz o no. |
| **Confirmar al vaciar la papelera** | Establece si se pide confirmación al usuario a la hora de vaciar la papelera. |

## Implicaciones de retirar la política ##

Se deja de vigilar que la configuración del navegador de archivos sea la indicada en la política.

## Reversibilidad ##

No es reversible puesto que no ofrece la posibilidad de restaurar los valores por defecto o recuperar un estado anterior.

## Ejemplo ##

Se desea fijar el comportamiento del explorador de ficheros para todos los usuarios de una unidad organizativa, según unas directrices establecidas.

Se instala la política **Navegador de archivos** en la unidad organizativa y se configura para obtener el comportamiento deseado. A partir de ese instante todos los usuarios tendrán una configuración idéntica. En caso de que haya excepciones se puede instalar la política a los usuarios seleccionados y fijar otros valores.
