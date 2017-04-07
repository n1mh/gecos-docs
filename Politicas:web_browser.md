# Navegador Web #

## Descripción ##

La política **Navegador Web** permite definir diversas opciones de configuración del navegador Mozilla Firefox como favoritos, página de inicio, plugins, certificados, etcétera. Todas las opciones están accesibles en la ventana **configuración del navegador**.

Esta política se aplica a unidades organizativas y usuarios.

Las opciones accesibles son las mismas que se presentan en el navegador abriendo about:config y la advertencia debe ser la misma: "úselas solo si está seguro de lo que está haciendo".

Políticas relacionadas: [cert](https://github.com/gecos-team/gecos-doc/wiki/Politicascert) y [network](https://github.com/gecos-team/gecos-doc/wiki/politicasnetwork).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-web_browser.png" width="600" alt="">

### Elementos del formulario ###

**Marcadores**

|  Parámetro  | Descripción |
| ----------- | ------------|
| Nombre | Nombre que tendrá el marcador elegido. |
| Uri | Dirección donde localizar el marcador. |

**Configuraciones**

|  Parámetro  | Descripción |
| ----------- | ------------|
| Clave | Dato para modificar alguna configuración del navegador web. |
| Tipo de valor | Tenemos tres tipos de datos para elegir, texto, numérico y booleano. |
| cadena | En el caso de que haya que introducir un dato tipo texto rellenaremos esta opción. |
| numero | En el caso de que haya que introducir un dato tipo numérico rellenaremos esta opción. |
| booleano | En el caso de que sea del tipo activar o desactivar marcaremos esta opción. |

**Plugins**

|  Parámetro  | Descripción |
| ----------- | ------------|
| Acción | Se podra instalar o desinstalar. |
| Nombre | Nombre que tendrá el plugin elegido. |
| Uri | Dirección donde localizar el plugin. |

## Implicaciones de retirar la política ##

Se deja de vigilar que la configuración del navegador indicada en la política siga presente.

## Reversibilidad ##

Puesto que no se hace un seguimiento de las opciones cambiadas en la configuración del navegador, esta opción no es reversible.

## Ejemplo ##

Se quiere configurar todos los puestos de una unidad organizativa para que Mozilla Firefox utilice la tecla de retroceso (`backspace`) para volver a la página anterior.

En la configuración de Mozilla Firefox se debe cambiar el parámetro `browser.backspace_action` y asignarle el valor numérico `0`.

Se instala la política **Navegador Web** en la unidad organizativa y se establece una nueva configuración con los siguientes datos:

* Clave: browser.backspace_action
* Tipo de valor: `number`
* Valor (sólo si el tipo de valor es un número): 0

Tras guardar y aplicar los cambios, el comportamiento del navegador en los puestos será el esperado.
