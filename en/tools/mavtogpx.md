# MAVTogpx
Exports the GPS data from a logfile and create a GPX file, which can be read by Google Earth.

Usage:
```
mavtogpx.py [-h] [--condition CONDITION]
            [--nofixcheck]
            LOG [LOG ...]
```
Positional arguments:
```
  LOG
```

Optional arguments:
```
  -h, --help
                        show this help message and exit
  --condition CONDITION
                        select packets by a condition
  --nofixcheck
                        don't check for GPS fix
```

Example:
```
mavtogpx.py 1.BIN

```

This tool generates a file with .gpx extension in the same directory. Now you can load this file in Google Earth.
