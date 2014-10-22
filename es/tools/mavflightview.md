# MAVFlightview
Este programa permite mostrar la posición GPS en una image. Se descarga la imagen de satélite (se peuden seleccionar diferentes servicios: Google, Microsoft, Yahoo entre otros) de la zona de vuelo y representa la trayectoria del vuelo.

Palabras reservadas: **Manual**, **AUTO**, **LOITER**, **FBWA**, **RTL**, **STABILIZE**, **LAND**, **STEERING**, **HOLD,** **ALT_HOLD**, **CIRCLE**, **POSITION**, **GUIDED**, **ACRO** and **CRUISE**.

Uso:
```
mavflightview.py [options]
```

Opciones:
```
-h, --help            show this help message and exit
  --service=SERVICE     tile service
  --mode=MODE           flight mode
  --condition=CONDITION
                        conditional check on log
  --mission=MISSION     mission file (defaults to logged mission)
  --fence=FENCE         fence file
  --imagefile=IMAGEFILE
                        output to image file
  --flag=FLAG           flag positions
  --rawgps              use GPS_RAW_INT
  --rawgps2             use GPS2_RAW
  --dualgps             use GPS_RAW_INT and GPS2_RAW
  --ekf                 use EKF1 pos
  --ahr2                use AHR2 pos
  --debug               show debug info
  --multi               show multiple flights on one map
```

Ejemplo:
Si quieres guardar el recorrido en un fichero necesitas añadir el flag `--imagefile <name>`

```bash
python mavflightview.py --imagefile output.jpg 25.BIN
```

Vas a ver una imagen similar. Una imagen de satélite con el recorrido del vuelo dibujado en diferentes colores (uno por cada modo de vuelo).

![viewALL](../erleimg/mavflighview/flightviewALL.jpg)

Si solo quieres ver un modo de vuelo necesitas aádir el flag  `--mode <MODE>`. Tienes que cambiar la palabra `MODE` por una de las palabras reservadas. 

```bash
python mavflightview.py --imagefile output.jpg --mode ALT_HOLD 25.BIN

```
En la siguiente imagen se puede ver el vuelo que corresponde al modo de vuelo *bloque de altitud*.

![viewALL](../erleimg/mavflighview/flightview.jpg)

