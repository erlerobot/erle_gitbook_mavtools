# MAVTomfile
This program converts a MAVLink log file to a MATLab mfile.

Usage:
```bash
mavtomfile.py [-h] [--condition CONDITION] [-o OUTPUT]                  [--types TYPES]
              [--dialect DIALECT]
              LOG [LOG ...]
```


positional arguments:
```
LOG
```

Optional arguments:
```bash
-h, --help            show this help message and exit
  --condition CONDITION
                        select packets by condition
  -o OUTPUT, --output OUTPUT
                        output filename
  --types TYPES         types of messages (comma separated)
  --dialect DIALECT     MAVLink dialect
```

Example:
```bash
mavtomfile.py 25.BIN
Processing 25.BIN
Creating m_25.m
```
