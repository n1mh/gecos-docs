# Administración de energía #

## Descripción ##

La política **Administración de energía** permite establecer el modo de operación de la CPU del equipo, modificando la frecuencia a la que opera la CPU y/o el apagado automático a cierta hora.

El escalado de frecuencia en la CPU sólo funciona en procesadores relativamente modernos.

Se puede aplicar a unidades organizativas y a equipos.

## Asistente ##

<img src="/gecos-team/gecos-doc/wiki/images/gecoscc/politicas/gecoscc-power.png" width="600" alt="px">

### Elementos del formulario ###

Cada una de las tres funciones de esta política puede aplicarse de manera independiente a las demás.

| Parámetro | Descripción |
| --------- | ----------- |
| **Control de la frecuencia de la CPU** | Los modos de frecuencia de CPU que admite son: `userspace` (frecuencia configurada manualmente por el usuario), `powersave` (funciona a la velocidad mínima), `conservative` (parecido a `ondemand` pero con cambios más suaves), `ondemand` (en función de la carga del sistema) y `performance` (a la máxima frecuencia). |
| **Suspensión automática de USB** | Elegiremos si los puertos USB se desactivaran para ahorrar consumo. ¡Ojo! en algunos equipos puede causar la pérdida de los primeros caracteres escritos tras una pausa. |
| **Hora** | Hora (en formato 24 horas) a la que apagar automáticamente el equipo. |
| **Minuto** | Minutos. |

## Implicaciones de retirar la política ##

Se deja de vigilar que la frecuencia de la CPU sea la indicada en la política y/o que el equipo de apague automáticamente a cierta hora.

## Reversibilidad ##

Aunque permite tener instalada la política sin configuracion, no almacena el estado anterior de la CPU por lo que no es posible volver al punto original de partida. Esta política no es reversible.

## Ejemplo ##

Se busca optimizar el rendimiento de un equipo puntual, rebajando el uso de la CPU y haciendo que se apague todos los días a las nueve de la noche.

Tras instalar la política **Administración de energía** en ese equipo se configura con los siguientes datos:

* Control de la frecuencia de la CPU
	* cambiar de `CPU frequency governor` a `powersafe`
* Hora: 21
* Minuto: 00

Guarde los cambios y encole la petición de actualización.

Vaya al puesto de trabajo y espere a que se actualice. Abra un terminal de comandos y teclee `cpufreq-info`. Compruebe que ahora la política de consumo de energía de la CPU (`current policy`) ha cambiado a `powersave`.

Compruebe que a las 21:00 el equipo se apaga automáticamente.
