# Conexión

MAVProxy permite conectarse a través del puerto USB o una conexión de red.

####--master
Especifica que puerto (serie, USB o conexión de red)se va a usar para comunicarse con el UAV.

####A través  USB

Si solo tenemos un APM conectado, el flags `--master` no es necesario. MAVProxy detectará el puerto automáticamente.
```
mavproxy.py --master=/dev/ttyUSB0
```
El *baudrare* tiene que coincidir con el de la conexión serie. Normalmente a 57600 baudios.

```
mavproxy.py --master=/dev/ttyUSB0 --baudrate=57600
```

####A través de la red
La dirección de conexión debe contener una IP y un puerto:

```
mavproxy.py --master=192.168.1.1:14550
```
