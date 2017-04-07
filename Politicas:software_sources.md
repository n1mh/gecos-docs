# Fuentes de software #

## Descripción ##

La política **Fuentes de software** permite añadir o eliminar repositorios de software de los equipos. Esto sirve para controlar el catálogo de aplicaciones disponibles para instalación.

Los repositorios que GECOS trae por defecto son:

|||||
| ------------ | ------------ | ------------ | ------------ |
| deb | [http://v2.gecos.guadalinex.org/ubuntu/](http://v2.gecos.guadalinex.org/ubuntu/) | precise | main restricted universe multiverse |
| deb | [http://v2.gecos.guadalinex.org/ubuntu/](http://v2.gecos.guadalinex.org/ubuntu/) | precise-updates | main restricted universe multiverse |
| deb | [http://v2.gecos.guadalinex.org/ubuntu/](http://v2.gecos.guadalinex.org/ubuntu/) | precise-security | main restricted universe multiverse |
| deb | [http://v2.gecos.guadalinex.org/ubuntu/](http://v2.gecos.guadalinex.org/ubuntu/) | precise-backports | main restricted universe multiverse |
| deb | [http://v2.gecos.guadalinex.org/min/](http://v2.gecos.guadalinex.org/min/) | maya | main upstream import backport |
| deb | [http://v2.gecos.guadalinex.org/gecos/](http://v2.gecos.guadalinex.org/gecos/) | v2 | main |

Políticas relacionadas: [auto_updates](https://github.com/gecos-team/gecos-doc/wiki/politicasReglas) y [package](https://github.com/gecos-team/gecos-doc/wiki/politicas#Package).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-softwaresources.png" width="600" alt="px">

### Elementos del formulario ###

|  Parámetro  | Descripción |
| ----------- | ------------|
| **Server key** | Clave del servidor. |
| **Uri** | Dirección de acceso al repositorio. |
| **Components** | Categorías en las que está organizado el repositorio: `main` (software soportado oficialmente), `restricted` (software soportado pero que no tiene una licencia completamente libre), `universe` (software mantenido por la comunidad), `multiverse` (software que no es libre). |
| **Repository key** | El servidor de claves. |
| **Sources** | Establece si añadir los fuentes de código también. |
| **Distribution** | Nombre de la distribución. |
| **Repository name** | Nombre del repositorio. |

## Implicaciones de retirar la política ##

Se deja de vigilar que los repositorios de software indicados en la política estén añadidos o eliminados según en cada caso.
