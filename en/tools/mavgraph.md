# MAVGraph

MAVGraph can graph any of the flight data. The commands are exactly the same as the graph module in MAVProxy.

Usage:

```
mavgraph.py 1.BIN "CTUN.BarAlt" "CTUN.Alt" "CTUN.DAlt"
```

### Flags
####--flightmode

This flag allows to show the different flight modes. This flag allows to show the different flight modes. The background of the graph changes depending on the flight mode. Here you can see the color code:

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

In the following graph It's possible to see two different colors. when the background color is green represents the stabilize mode (at the beginning and in the end of the graph, the copter takes off and lands). When the background is red the copter is in altitude hold mode. You can check the color with the description above.

![modovuelo](../en/erleimg/mavgraph/flightmodes.png)

