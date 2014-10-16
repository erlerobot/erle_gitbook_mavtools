# GPS

Cuando hay un error en los modos que usan el GPS puedes pensar que APM:Copter que de reprente tiene una posición incorrecta y volar de una forma agresica para corregir ese error. Estos fallos aparecen en los logs como un decremente en el número de satélites visibles y el decremente de `hdop`.

```bash
mavgraph.py 30.BIN "GPS.Lat" "GPS.Lng" --flightmode=apm
```

![gps_lostsignal](../erleimg/GPS/GPS_lostsignal.png)

Si estas usando los logs para representar el GPS puedes mostrar *eph* y el *número de satélites visibles*. Un valor de hdop de 1.5 o inferior es bueno. Mayor de 2.0 indica una mala posición. Un cambio significante en estos dos valores a menudo viene acompañado de un cambio en la posición del GPS. En los logs estos mensajes del GPS de pueden encontrar en  “HDop” y “NSats”.

![NSats](../erleimg/GPS/GPS_NSats.png)
