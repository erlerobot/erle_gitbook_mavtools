# Comandos del sistema

####reboot
Reinicia APM

####setup
Va al modo configuración de APM

####rc
Sobreescribe el canal de entrada de radiofrecuencia. El valor permanece hasta que se introduce un valor de -1. Usa la forma `rc <chan value>`. Utiliza `all` para poner todos los canales al mismo valor:

```
rc 1 1000
rc all -1
```

####time
Muestra el valor actual del autopiloto, si lo soporta. El tiempo entre paréntesis es el tiempo de la estción de tierra.

####link
Muestra el estado del enlace de telemetría.

####script
Ejecuta un fichero de texto que contiene comando de MAVProxy

####status
Muestra los últimos paquetes recibidos desde el autopiloto. Útil para la lectura del estado de la UAV.