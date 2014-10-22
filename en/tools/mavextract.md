# MAVExtract
This script allows to extract one flight mode from the rest of the log. If you change the flight mode several times this program generates a new `.BIN` file for each one.

Reverse words: **Manual**, **AUTO**, **LOITER**, **FBWA**, **RTL**, **STABILIZE**, **LAND**, **STEERING**, **HOLD,** **ALT_HOLD**, **CIRCLE**, **POSITION**, **GUIDED**, **ACRO** and **CRUISE**.

To extract a specific flight mode yo have to use the flag `--mode MODE`. You have to change the word `MODE` for one of the reverse words.

Usage:
```
mavextract.py [-h] [--no-timestamps] [--robust]                         [--condition CONDITION]
              [--mode MODE]
              LOG [LOG ...]
```

Positional arguments:
```
LOG
```

Optional arguments:
```
  -h, --help            show this help message and exit
  --no-timestamps       Log doesn't have timestamps
  --robust              Enable robust parsing (skip over bad data)
  --condition CONDITION
                        select packets by condition
  --mode MODE           mode to extract
```

Example:
````
mavextract.py 1.BIN --mode LAND
Processing 2/98.BIN
Creating LAND1.bin
```
