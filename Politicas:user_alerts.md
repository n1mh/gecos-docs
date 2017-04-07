# Alertas de usuario #

## Descripción ##

La política **Alertas de usuario** permite configurar mensajes de advertencia para usuarios. La alerta aparecerá a los 5 minutos de la sincronización del puesto con el Centro de Control. Si no se retira la política, volverá a aparecer la notificación al cabo de un año exacto.

Si se edita la política (sin necesidad de modificar nada) y se aplican los cambios, o si se quita y se vuelve a poner la política, volverá a presentarse la alerta. Esencialmente se trata de una política de un solo uso, que no vigila ninguna configuración o comportamiento del puesto.

Esta política se aplica a unidades organizativas y usuarios.

Políticas relacionadas: [local_groups](https://github.com/gecos-team/gecos-doc/wiki/Politicaslocal_groups) y [local_users](https://github.com/gecos-team/gecos-doc/wiki/politicasUsuarios).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-user-alerts.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **Cuerpo** | Descripción a mostrar en el mensaje de alerta. |
| **Titulo** | Cabecera del mensaje de alerta. |
| **Urgencia** | Tiempo que durara el mensaje mostrado. |
| **icono** | Icono a mostrar en el mensaje visual. |

## Implicaciones de retirar la política ##

La alerta no se reproducirá al cabo de un año.

## Reversibilidad ##

Esta política es reversible puesto que no modifica el estado del ordenador.

## Ejemplo ##

Debido a un corte en la conexión a internet se quiere mostrar un mensaje informativo a todos los usuarios activos.

En la unidad organizativa se instala la política **Alertas de usuario** y se configura con los siguientes datos:

Cuerpo: A partir de las 17 horas y durante 10 minutos se procederá a cortar la conexión a internet para mejoras en la red. Disculpen las molestias.
Titulo: Corte en la conexión a internet
Urgencia: Critical
icono: info

Guardar y aplicar la política.

En los puestos, a los pocos minutos, comenzarán a mostrarse los avisos a los usuarios activos.
