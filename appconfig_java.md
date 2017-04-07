# Configuración de Java #

## Descripción ##

La política **Configuración de Java** establece una configuración específica para el cliente Java.

Esta política se aplica a unidades organizativas y equipos.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/appconfig_java.png" width="600" alt="px">

### Elementos del formulario ###

|  Parámetro  | Descripción |
| ----------- | ------------|
| **Versión de Java** | Especifica la versión de Java a emplear escribiendo la ruta absoluta al directorio del JRE. |
| **Plugins versión de Java** | Especifica la ruta absoluta al directorio del JRE con los nuevos plugins |
| **Nivel de Seguridad** | Fija el nivel de seguridad que el cliente Java tendra. Los valores son: medio (`MEDIUM`), alto (`HIGH`) y muy alto (`VERY_HIGH`) |
| **Utilizar lista de revocación de certificados** | Configurar el cliente Java para utilizar la lista de revocación de certicados |
| **¿Mostrar advertencia de incompatibilidad de host para el certificado?** | Activa la opción de que se muestre un aviso cuando el certificado del servidor al que se conecta no sea correcto. |
| **Verificación de la seguridad de la combinación de código** | Activa la verificación de seguridad del código. |
| **Activar o desactivar el protocolo de estado de certificados en linea** | Activa el protocolo de estado de certificados en linea. |
| **Otras propiedades de configuración** | Permite introducir duplas Clave-Valor no cubiertas en el formulario. Se pueden añadir tantas como sea necesiario. |

## Implicaciones de retirar la política ##

Se deja de vigilar que la configuración del cliente Java indicada en la política siga presente.

## Reversibilidad ##

Puesto que no almacena el estado anterior a la instalación de la política y no permite volver a ese punto, esta política no es reversible.

## Ejemplo ##

Se fija la necesidad de tener un cliente Java específico (`jre1.8.0_101`) y una configuración común en todos los puestos.

Mediante un paquete de software se instala en todos los equipos la versión estipulada del cliente Java. Se utiliza el directorio `/opt/jre1.8.0_101`.

Se instala la política **Configuración de Java** en la unidad organizativa y se configura con los siguientes datos:

* Versión de Java: `/opt/jre1.8.0_101`
* Plugins versión de Java:
* Nivel de Seguridad: HIGH
* Utilizar lista de revocación de certificados: activado
* ¿Mostrar advertencia de incompatibilidad de host para el certificado?: activado
* Verificación de la seguridad de la combinación de código: HIDE_RUN
* Activar o desactivar el protocolo de estado de certificados en linea: activado
* Otras propiedades de configuración:

Tras guardar y activar, los puestos contarán con una versión concreta del cliente Java y configuración común.
