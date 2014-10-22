# MAVParms
Encuentra los parámetros de APM en un archivo de registro y los muestra en la consola.

Uso:
```bash
mavparms.py [-h] [-c] LOG [LOG ...]
```

Argumentos posicionales:
```bash
    LOG
```
Argumentos opcionales:
```bash
  -h, --help     show this help message and exit
  -c, --changes  Show only changes to parameters.
```
Ejemplo:
```bash
mavparms.py 1.BIN
```

Puedes ver todos los parámetros de tu vuelo:

```
...
RATE_RLL_IMAX   1000.000000
RATE_RLL_P      0.090000
RATE_YAW_D      0.000000
RATE_YAW_I      0.020000
RATE_YAW_IMAX   1000.000000
RATE_YAW_P      0.200000
RC10_DZ         0.000000
RC10_FUNCTION   0.000000
RC10_MAX        1900.000000
RC10_MIN        1100.000000
RC10_REV        1.000000
RC10_TRIM       1500.000000
RC11_DZ         0.000000
RC11_FUNCTION   0.000000
RC11_MAX        1900.000000
RC11_MIN        1100.000000
RC11_REV        1.000000
RC11_TRIM       1500.000000
RC1_DZ          30.000000
RC1_MAX         2016.000000
RC1_MIN         991.000000
RC1_REV         1.000000
RC1_TRIM        1503.000000
RC2_DZ          30.000000
RC2_MAX         2016.000000
RC2_MIN         991.000000
RC2_REV         -1.000000
RC2_TRIM        1506.000000
RC3_DZ          30.000000
RC3_MAX         2016.000000
RC3_MIN         991.000000
RC3_REV         1.000000
RC3_TRIM        991.000000
RC4_DZ          40.000000
RC4_MAX         2016.000000
RC4_MIN         993.000000
RC4_REV         1.000000
RC4_TRIM        1500.000000
RC5_DZ          0.000000
RC5_FUNCTION    0.000000
RC5_MAX         1504.000000
RC5_MIN         1500.000000
RC5_REV         1.000000
RC5_TRIM        1502.000000
RC6_DZ          0.000000
RC6_FUNCTION    0.000000
RC6_MAX         1504.000000
RC6_MIN         1500.000000
RC6_REV         1.000000
RC6_TRIM        1502.000000
RC7_DZ          0.000000
RC7_FUNCTION    0.000000
RC7_MAX         1504.000000
RC7_MIN         1500.000000
RC7_REV         1.000000
RC7_TRIM        1502.000000
RC8_DZ          0.000000
RC8_FUNCTION    0.000000
RC8_MAX         1504.000000
RC8_MIN         1500.000000
RC8_REV         1.000000
RC8_TRIM        1502.000000
...
```
