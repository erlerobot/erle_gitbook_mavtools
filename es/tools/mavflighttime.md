# MAVFlighttime
Imprime el tiempo total de permanencia en el aire. Tenga en cuenta que un umbral de 3 m/s define la diferencia entre el tiempo de vuelo y el tiempo en tierra. Esto se puede cambiar por el argumento --groundspeed.

Uso:
```bash
mavflighttime.py [-h] [--condition CONDITION]
                 [--groundspeed GROUNDSPEED]
                 LOG [LOG ...]
```
Argumentos posicionales:
```bash
  LOG
```

Argumentos opcionales:
```bash
  -h, --help            show this help message and exit
  --condition CONDITION
                        condition for packets
  --groundspeed GROUNDSPEED
                        groundspeed threshold
```
Ejemplo
```
mavflighttime.py 1.BIN
```
Puedes ver el resumen del vuelo:

```
In air at Thu Oct  9 16:56:51 2014 (percent 27% groundspeed 3.6)
On ground at Thu Oct  9 16:56:52 2014 (percent 27.5% groundspeed 2.3  time=1.0 seconds)
In air at Thu Oct  9 17:02:41 2014 (percent 85% groundspeed 3.1)
On ground at Thu Oct  9 17:02:41 2014 (percent 85.0% groundspeed 2.3  time=0.0 seconds)
In air at Thu Oct  9 17:03:22 2014 (percent 95% groundspeed 3.0)
On ground at Thu Oct  9 17:03:22 2014 (percent 94.9% groundspeed 2.6  time=0.0 seconds)
Flight time : 0:01
Total time in air: 0:01
Total distance trevelled: 258.3 meters
```
