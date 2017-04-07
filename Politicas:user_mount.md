# Montaje de unidades externas #

## Descripción ##

La política **Montaje de unidades externas** permite establecer si un usuario puede o no acceder a **unidades de almacenamiento externas** (pendrives, discos USB, otras particiones del disco, etc). Esta política no afecta al montaje de unidades de almacenamiento en red.

En un puesto GECOS vinculado a un Centro de Control, el usuario no puede montar unidades externas hasta no concederle este permiso.

Políticas relacionadas: [folder_sharing](https://github.com/gecos-team/gecos-doc/wiki/Politicasfolder_sharing).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-usermount.png" width="600" alt="px">

### Elementos del formulario ###

|  Parámetro  | Descripción |
| ----------- | ------------|
| **¿Puede montar?** | Casilla que establece si el usuario puede acceder a unidades de almacenamiento externas. |

## Implicaciones de retirar la política ##

Se deja de vigilar si el usuario puede acceder o no a unidades de almacenamiento externas. El usuario queda con la autorización que tenía en el momento de retirar la política.

## Reversibilidad ##

Esta política es reversible puesto que siempre se puede volver al estado inicial que es no permitir el montaje de unidades externas a los usuarios.

## Ejemplo ##

Para permitir que los usuarios de una unidad organizativa utilicen dispositivos de almacenamiento en sus puestos basta con instalar la política **Montaje de unidades externas** y activar la opción. En unos minutos podrán montar las unidades externas y utilizarlas.
