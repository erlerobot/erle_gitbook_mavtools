# MAVTomfile
Este programa convierte un fichero de log de MAVLink en un fichero `.m` de Matlab.

Usage:
```bash
mavtomfile.py [-h] [--condition CONDITION] [-o OUTPUT]                  [--types TYPES]
              [--dialect DIALECT]
              LOG [LOG ...]
```

Argumentos posicionales:
```
LOG
```

Argumentos opcionales:
```bash
-h, --help            show this help message and exit
  --condition CONDITION
                        select packets by condition
  -o OUTPUT, --output OUTPUT
                        output filename
  --types TYPES         types of messages (comma separated)
  --dialect DIALECT     MAVLink dialect
```

Ejemplo:
```bash
mavtomfile.py 25.BIN
Processing 25.BIN
Creating m_25.m
```
