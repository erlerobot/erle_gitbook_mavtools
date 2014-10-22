# Scripts
MAVProxy es capaz de ejecutar script (de comandos de MAVProxy) en su inicio. Esto puede ayudarte en el esfuerzo de (re)configurar el entorno de MAVProxy en cada vuelo.

El script (mavinit.scr) puede ser situado en el directoria del aeronave (ie. MAVProxy/Aircraftname/mavinit.scr) conteniendo los parámetros. Cualquier comando de MAVProxy puede estar dentro de él. Tenga en cuenta que la opción `--aircraftà debe ser utilizado, con el objetivo de que MAVProxy para encontrar la secuencia de comandos en el directorio de aeronave apropiada.


Alternativamente, un .mavinit.scr se puede colocar en el directorio home del usuario (es decir. /home/nombredeusuario en Linux o /Users/nombredeusuario en MACOS) y se cargará con MAVProxy independientemente de la opción `--aircraft`.

También puedes cargar un script introduciendo:

```
script mavinit.scr
```

En este script en particular, los alias se utilizan como accesos directos a los comandos comunes.

Por ejemplo:
```
@alias add grp g degrees(ATTITUDE.roll) degrees(ATTITUDE.pitch)
```
en el mavinit.scr permitirá al usuario para representar gráficamente el *pitch*  y el *roll*en grados escribiendo:

```
grp
```

en lugar de:

```
graph degrees(ATTITUDE.roll) degrees(ATTITUDE.pitch)
```
