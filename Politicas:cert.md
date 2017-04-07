# Gestión de certificados #

## Descripción ##

La política **Gestión de certificados** añade certificados digitales al equipo que pueden ser CA (certificado raíz de una autoridad certificadora) o JKS (almacenes de claves de Java). Al configurar nuevos certificados, éstos se añaden a los almacenes de claves correspondientes.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-cert.png" width="600" alt="px">

### Elementos del formulario ###

Las opciones mostradas en el formulario no son excluyentes.

La primera parte del formulario es para los certificados a emplear por Java de forma independiente, es decir, cuando no se utiliza embebido en un navegador, mientras que el segundo grupo de campos se emplea con las entidades certificadoras a añadir a Mozilla Firefox. En ambas partes se pueden especificar tantos certificados o almacenes como sea necesario.

| Parámetro | Descripción |
| ----------- | ------------|
| **Almacenes de claves de Java** | Ruta absoluta hasta el fichero almacén de claves de Java (JKS). |
| **Certificados raíces de Autoridades de Certificación (CA) - Nombre** | Nombre que se le dará al certificado digital de la entidad certificadora en Mozilla Firefox para identificarlo. |
| **Certificados raíces de Autoridades de Certificación (CA) - URI del certificado** | Dirección URI con la ruta hasta el certificado. |

## Implicaciones de retirar la política ##

Al retirar la política únicamente se deja de vigilar que los certificados digitales se gestionen, aunque los certificados instalados permanecen en el sistema.

## Reversibilidad ##

Esta política es reversible puesto que el formulario permite el borrado de todos los certificados y almacenes JKS que tuviese configurado, volviendo así al punto de partida.

## Ejemplo ##

Al acceder a [la web del PortaFirmas de la Junta de Andalucía](https://ws199.juntadeandalucia.es/CentroDeFirmas/index.htm?cid=62171) se muestra una advertencia del navegador porque la conexión establecida con la web no es segura. Esto se debe a que la entidad certificadora emisora del certificado (la Fábrica Nacional de Moneda y Timbre) que emplea dicha página web no está en el sistema y, consecuentemente, los certificados que emite son marcados como no seguros.

Para solucionarlo se debe instalar en las máquinas GecOS la política **Gestión de certificados** con el certificado **FNMT-RCM** emitido por la **Fábrica Nacional de Moneda y Timbre**. Una vez incorporada la política se configura el certificado con los siguientes datos:

* **Nombre**: FNMT-RCM
* **URI del certificado**: https://www.sede.fnmt.gob.es/documents/11614/116099/AC_Raiz_FNMT-RCM_SHA256.cer

En el ordenador cliente, tras la instalación de la política se debe reiniciar el navegador Mozilla Firefox en caso de que estuviese en uso para refrescar la lista de entidades certificadoras.

Al acceder de nuevo a la web del PortaFirmas no se mostrará el mensaje de advertencia.
