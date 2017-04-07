# Carpeta para sincronizar #

## Descripción ##

La política **Carpeta para sincronizar** permite configurar un cliente `owncloud` para sincronizar un directorio local con el servidor especificado.

Políticas relacionadas: [local_file](https://github.com/gecos-team/gecos-doc/wiki/politicasLocalFile).

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-foldersync.png" width="600" alt="px">

### Elementos del formulario ###

| Parámetro | Descripción |
| --------- | ----------- |
| **URL de Owncloud** | URL del servidor `owncloud` donde realizar la sincronización de ficheros.

## Implicaciones de retirar la política ##

Se deja de vigilar que los contenidos del usuario y la unidad en red estén sincronizados.

## Reversibilidad ##

La política es reversible puesto que permite que esté instalada y con el campo **URL de Owncloud** vacío.

## Ejemplo ##
