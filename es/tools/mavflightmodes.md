# MAVFlightmodes
Imprime la fecha, hora y el nombre de cada cambio de modo de vuelo en un archivo de log.

Uso:
```bash
mavflightmodes.py [-h] LOG [LOG ...]
```

Argumentos posicionales:
```bash
  LOG
```
Argumentos opcionales:
```bash
  -h, --help  show this help message and exit
```

Ejemplo:

```
mavflightmodes.py 1.BIN
```

Salida:

```
Thu Oct  9 16:54:56 2014 MAV.flightmode=STABILIZE    (MAV.timestamp=1412866496 0%)
Thu Oct  9 16:55:19 2014 MAV.flightmode=ALT_HOLD     (MAV.timestamp=1412866519 6%)
Thu Oct  9 17:03:15 2014 MAV.flightmode=STABILIZE    (MAV.timestamp=1412866995 93%)

Time per mode:
ALT_HOLD     0:07:55 89.99%
STABILIZE    0:00:52 10.01%
```
