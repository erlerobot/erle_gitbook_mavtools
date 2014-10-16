# MAVGraph
MAVGraph permite representar cualquier dato de vuelo. El comando es exactamente el mismo que el modulo `graph` en MAVProxy.

Uso:

```
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

