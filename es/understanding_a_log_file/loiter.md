#LOITER

El modo Loiter intenta mantener de manera automática la posición actual, en orientación y altura. El piloto puede volar el vehículo en el modo Loiter como si estuviera en manual. Soltando los sticks se mantendrá dicha posición.

Una buena posición GPS necesita de **baja interferencia magnética** de la brújula y **bajas vibraciones** para conseguir un buen redimiento en el modo Loiter.

El modo Loiter incorpora el controlador de altitud del modo control de altitud. Los detalles para ajustar el modo *AltHold* están en [esta página](altitude_hold.md)

##Controles
El piloto puede controlar la posición del vehículo con los sticks. En AC3.1 (y superiores) se puede armar en el modo Loter pero solo si el GPS tiene en bloqueo 3D y el **HDop devuelve un valor de 2 o inferior**.

- La posición horizontal puede ajustarse con los stick que controlan el *Pitch* y el *Roll* con la velocidad por defecto de 5m/s. Cuando el piloto suelta los sticks el vehículo se parará.
- La altitud se controla con el stick del Throttle como en el modo [AltHold](altitude_hold.md).
- La orientación se puede modificar con el stick de control del *Yaw*

## Puesta a punto

La máxima velocidad horizontal del vehículo durante el modo loiter puede ajustar con el parámetro de velocidad Loiter (**WPNAV_LOIT_SPEED**). El valor se expresa en cm/s desde 500 a 5m/s. El máximo valor de aceleración durante el modo Loiter siempre es la mitad de la velocidad Loiter.

El valor P del controlador PID se utilizada para convertir el error de posición horizontal (por ejemplo la diferencia entre la posición deseada y la posición actual) a una velocidad deseada hacia la posición de destino. **Generalmente no requiere de ajuste**.


## Verificando el rendimiento de Loiter con logs

Revisando el redimiento de la posición horizontal es la mejor manera, para ello es necesario descargar el log de vuelo. Representa los campos del mensaje **NTUN**: DesVelX vs VelX y DesVelY vs VelY. Un buen resultado es que la velocidad actual siga a la velocidad deseada como se muestra en las gráficas inferiores. X = latitud (positivo = moviendose hacia el norte, negativo = Sur), Y = longitud (positivo = Este, negativo = Oeste).

```
mavgraph.py $LOITER1.BIN "NTUN.DVelX" "NTUN.VelX" --flightmode=apm
```

![velX](../erleimg/LOITER/loiterX.png)

```
mavgraph.py $LOITER1.BIN "NTUN.DVelY" "NTUN.VelY" --flightmode=apm
```

![velY](../erleimg/LOITER/loiterY.png)

Para revisar el redimiento del control de altitud es el mismo que [AltHold](altitude_hold.md).

## Problemas comunes

Como se menciona arriba, el modo Loiter incorpora el controlador de altutid de [AltHold](altitude_hold.md).

- El vehículo despega en la dirección incorecta cuando se entra en el modo loiter. Si el error de la brújula es mayor de 90 grados. Intenta las sugerencias de aajo para resolverlo.
- El vehículo esta funcionando correctamente en el modo Loiter y de repente se mueve en dirección incorrecta. Esto es causado por un *glitch* del GPS. No hay una protección fiable al 100% contra ésto lo que significa que el piloto debe estar siempre listo para tomar el control del vehículo. Ántes de despegar es bueno comprobar tener un buen valor HDop del GPS, puede ayudar reducir los parámetros GPSGLITCH_RADIUS y/o GPSGLITCH_ACCEL.
