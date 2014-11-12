# Rendimiento

EL rendimiento del APM corre en una maquina Linux y puede ser monitorizado utilizando el parámetro `SCHED_DEBUG`.

De acuerdo con la [wiki](http://copter.ardupilot.com/wiki/arducopter-parameters/#Scheduler_debug_level_SCHED_DEBUG):

```
Ajusta el parámetro a un valor distinto de cero para ver los mensajes de depuración de planificación. Cuando se configura para mostrar los "Slips" el planificador mostrará una mensaje cada vez que se retrasa una tarea programada debido a un exceso de carga de la CPU. Cuando se configura el "Overruns" el planificador mostrará un mensaje cada vez que una tarea tarda más que el límite de los prometido según la tabla de tareas.
```

|Valor	| Significado |
|-----|-----|
|0	|Desabilitado|
|2	|Muestra *Slips*|
|3	|Muestra *Overruns*|


Configura el parámetro utilizando `param set SCHED_DEBUG 3` y obtendrás una salida como esta:

```bash
Scheduler overrun task[15] (34/20)
Scheduler overrun task[16] (26/20)
PERF: 4/1000 21647
PERF: 3/1000 23464
Flight battery warning
PERF: 5/1000 21938
Scheduler overrun task[5] (15/10)
PERF: 4/1000 23464
PERF: 4/1000 21506
Scheduler overrun task[15] (24/20)
PERF: 5/1000 22517
PERF: 3/1000 23606
Scheduler overrun task[5] (14/10)
Scheduler overrun task[16] (23/20)
PERF: 4/1000 21146
Flight battery warning
```

## Entendiendo la salida

### PERF

```
PERF: 4/1000 23464
```
Se debe de entender como:
should be understood as:
>4 de 1000 tomó más tiempo de los esperado

### Overrun task

```
Scheduler overrun task[16] (23/20)
```
> La tarea 16 ejecuto en 23 frente a los 20 tenía que ejecutar.

Revisa la [web](http://dev.ardupilot.com/wiki/code-overview-scheduling-your-new-code-to-run-intermittently/) para entender más sobre las tareas.
