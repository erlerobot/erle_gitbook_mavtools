# MAVTogpx
Exporta los puntos GPS en un archivo de registro en el formato GPX, que puede ser leído por Google Earth.

Uso:

```bash
mavtogpx.py [-h] [--condition CONDITION]
            [--nofixcheck]
            LOG [LOG ...]
```

Argumentos posicionales:
```bash
  LOG
```

Argumentos opcionales:
```bash
  -h, --help            
                        show this help message and exit
  --condition CONDITION
                        select packets by a condition
  --nofixcheck
                        don't check for GPS fix
```

Ejemplo

```bash
mavtogpx.py 1.BIN

```

Esta herramienta genera un archivo con extensión .gpx en el mismo directorio. Ahora se puede cargar este archivo en Google Earth.
