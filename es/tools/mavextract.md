# MAVExtract
Este script permite estraer un modo de vuelo del resto del log. Si cambias varias veces el modo de vuelo este programa genera un fichero `.BIN` por cada uno.

Palabras reservadas: **Manual**, **AUTO**, **LOITER**, **FBWA**, **RTL**, **STABILIZE**, **LAND**, **STEERING**, **HOLD,** **ALT_HOLD**, **CIRCLE**, **POSITION**, **GUIDED**, **ACRO** and **CRUISE**.

Para extraer un modo de vuelo especifico tienes que usar el flag `--mode MODE`. Tienes que sustituir la palabra `MODE` por una de las palabras reservadas.


Uso:
```
mavextract.py [-h] [--no-timestamps] [--robust]                         [--condition CONDITION]
              [--mode MODE]
              LOG [LOG ...]
```

Argumentos posicionales:
```
LOG
```

Argumentos opcionales:
```
  -h, --help            show this help message and exit
  --no-timestamps       Log doesn't have timestamps
  --robust              Enable robust parsing (skip over bad data)
  --condition CONDITION
                        select packets by condition
  --mode MODE           mode to extract
```

Ejemplo:
````
mavextract.py 1.BIN --mode LAND
Processing 2/98.BIN
Creating LAND1.bin
```
