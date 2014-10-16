# ¿Dónde puede encontrar un fichero de log?


Los *log* de vuelo se almacenan en `rootfs`. A fichero de log se genera cuando el autopiloto se inicia y el sistema es armado.

##SDCARD
Si conectamos la tarjeta SD a nuestro PC e introducimos el comando `mount` podemos ver que tenemos montado en nuestro sistema. Por ejemplo en `media/rootfs`
Haciendo :
```
cd /media/rootfs
```
Si no situamos en la paritición `rootfs`. Los logs se almacenan en `/var/APM/logs`.

```
cd /var/APM/logs
```
Aquí puedes encontrar todos los logs de `APMrover2`, `ArduCopter` o `ArduPlane` y un fichero llamado `lastlog.txt`.
```
less lastlog.txt
```
muestra el nombre del último log, supongamos que es `5.BIN`. Ahora podemos copiarlo en la carpeta `Logs` de nuestro *home*, haciendo:
```
cp 5.BIN ~/Logs
```

##SSH

Podemos conectarnos a la placa mediante SSH a tráves de USB or Wifi y navegar por el sistema de ficheros para encontrar un log interesante.

Si quieres conectarte con la placa usando el USB. Tienes que revisar la IP porque el servidor DHCP en ocasiones da problemas. Cuando conectas la placa se crea una nueva interfaz de red. Es posible comprobar la interfaz con el comando `ifconfig`. Para forzar la IP tienes que introducir en la shell (en este caso `eth2` es la interfaz de red creada por la Beaglbone):

```
sudo ifconfig eth2 192.168.7.2
```

Ahora, te puedes conectar a la placa por SHH:

```
ssh root@192.168.7.2
```

o por wifi:

```
ssh root@111.0.0.1
```

Es posible copiado un fichero utilizando `scp` desde tu ordenados:

```
scp root@192.168.7.2:/var/APM/logs/1.BIN ~/LOGS
```

#Sube tu log

Los logs generalmente son añadidos a [https://github.com/erlerobot/logs](https://github.com/erlerobot/drones_logs)
