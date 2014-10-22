# MAVFlightmodes
Prints out the timestamp and name of each flight mode change in a logfile.

Usage:
```bash
mavflightmodes.py [-h] LOG [LOG ...]
```

Positional arguments:
```bash
  LOG
```
Optional arguments:
```bash
  -h, --help  show this help message and exit
```

Example:

```bash
mavflightmodes.py 1.BIN
```

Output:

```bash
Thu Oct  9 16:54:56 2014 MAV.flightmode=STABILIZE    (MAV.timestamp=1412866496 0%)
Thu Oct  9 16:55:19 2014 MAV.flightmode=ALT_HOLD     (MAV.timestamp=1412866519 6%)
Thu Oct  9 17:03:15 2014 MAV.flightmode=STABILIZE    (MAV.timestamp=1412866995 93%)

Time per mode:
ALT_HOLD     0:07:55 89.99%
STABILIZE    0:00:52 10.01%
```
