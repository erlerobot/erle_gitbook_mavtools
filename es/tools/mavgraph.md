# MAVGraph
MAVGraph permite representar cualquier dato de vuelo. El comando es exactamente el mismo que el modulo `graph` en MAVProxy.

Uso:
```bash
mavgraph.py [-h] [--no-timestamps] [--planner] [--condition CONDITION]
                   [--labels LABELS] [--legend LEGEND] [--legend2 LEGEND2]
                   [--marker MARKER] [--linestyle LINESTYLE] [--xaxis XAXIS]
                   [--multi] [--zero-time-base] [--flightmode FLIGHTMODE]
                   [--output OUTPUT]
                   <LOG or FIELD> [<LOG or FIELD> ...]
```

Argumentos posicionales:
```bash
<LOG or FIELD>
```

Argumentos opcionales:
```bash
  -h, --help            show this help message and exit
  --no-timestamps       Log doesn't have timestamps
  --planner             use planner file format
  --condition CONDITION
                        select packets by a condition
  --labels LABELS       comma separated field labels
  --legend LEGEND       default legend position
  --legend2 LEGEND2     default legend2 position
  --marker MARKER       point marker
  --linestyle LINESTYLE
                        line style
  --xaxis XAXIS         X axis expression
  --multi               multiple files with same colours
  --zero-time-base      use Z time base for DF logs
  --flightmode FLIGHTMODE
                        Choose the plot background according to the active
                        flight mode of the specified type, e.g.
                        --flightmode=apm for ArduPilot or --flightmode=px4 for
                        PX4 stack logs. Cannot be specified with --xaxis.
  --output OUTPUT       provide an output format
```

Ejemplo
```bash
mavgraph.py 1.BIN "CTUN.BarAlt" "CTUN.Alt" "CTUN.DAlt"
```

### Flags
####--flightmode

Este flag permite mostrar los diferentes modos de vuelo.El color de fondo de la gráfica cambia dependiendo del modo de vuelo. A continuación puedes ver el código de colores:

```
    'MANUAL'    : (1.0,   0,   0),
    'AUTO'      : (  0, 1.0,   0),
    'LOITER'    : (  0,   0, 1.0),
    'FBWA'      : (1.0, 0.5,   0),
    'RTL'       : (  1,   0, 0.5),
    'STABILIZE' : (0.5, 1.0,   0),
    'LAND'      : (  0, 1.0, 0.5),
    'STEERING'  : (0.5,   0, 1.0),
    'HOLD'      : (  0, 0.5, 1.0),
    'ALT_HOLD'  : (1.0, 0.5, 0.5),
    'CIRCLE'    : (0.5, 1.0, 0.5),
    'POSITION'  : (1.0, 0.0, 1.0),
    'GUIDED'    : (0.5, 0.5, 1.0),
    'ACRO'      : (1.0, 1.0,   0),
    'CRUISE'    : (  0, 1.0, 1.0)
```

En la siguiente gráfica se ven dos colores. Cuando el color de fondo es verde representa el modo `stabilize` (en el principio de la gráfica y al final, es donde el helicoptero despega y aterriza). Cuando el color de fondo es rojo el helicoptero esta en modo `ALT_HOLD`. Puedes comprobrar los colores con la descripción de arriba. 

![modovuelo](../erleimg/mavgraph/flightmodes.png)

