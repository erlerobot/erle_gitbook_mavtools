# Entendiendo un fichero de log

Hay dos maneras de guardar un los datos de vuelo con ArduCopter. Con algunas excepciones, estos dos métodos guardar información muy similar pero de diferentes formas:

+ **Datos de vuelo en la memoria flash** utiliza la memoria de la BeagleBoard que se puede descargar después del vuelo. En *ArduPlane* y *ArduRover* los datos de vuelo se crean al iniciarse. En **ArduCopter* se crean después de armar el vehículo**.
+ **Datos de telemetría** (también conocidos como "tlogs") son guardados por MAVProxy ( o otra estación de control como : Mision Planner, QGroundControl, etc) cuando se conectar APM a tu ordenador mediante un enlace de telemetría. 

##Datos de vuelo

###Detalles de los mensajes(APM:Copter especificamente)
+ **ATT** (información de altitud)
 + DesRoll: ángulo de *roll* deseado por el piloto en centi-grados (izquierda es negativo, y derecha es positivo). 
 + Roll: El *roll* actual del vehiculo en centi-grados (izquierda es negativo, y derecha es positivo).
 + DesPitch: ángulo *pitch* deseado por el piloto en centi-grados (izquierda es negativo, y derecha es positivo). 
 + Pitch: El *pitch* actual del vehículo en centi-grados (izquierda es negativo, y derecha es positivo). 
 + DesYaw: El ángulo *yaw* deseado en centi-grados.
 + Yaw: El ángulo actual del vehículo en centi-grados con 0 = north.
+ **IMU** (información de acelerómetro y giróscopo):
 + GyrX, GyrY, GyrZ: La información en bruto de giróscopo en grados/segundos.
 + AccX, AccY, AccZ: La información en bruto de los acelerómetros expresado en m/s/s.
+ **GPS**
 + Lat: Latitud de acuerdo con el GPS.
 + Lng: Longitud de acuerdo con el GPS
+ **RCOUT** (salida pwm ): RC1, RC2, etc :los comandos pwm se envían del controlar de vuelo a los esc/motores/Radio control.
+ **CTUN** (acelerador e información de atitud):
 + Alt: La altitud expresada en metros
 + BarAlt: La altitud sobre el suelo de acuerdo con el barómetro.
 + DAlt: La altitud deseada mientrás se está en modo *AltHold*, *Loiter*, *RTL* o Auto*
+ **BARO** (información del barómetro):
 + Alt (0.0602620765567) ?
 + Press : (101291.015625) ?
 + Temp : (25.57) Temperatura en (º C).
 + CRt : (0.0213998798281) ?
+ **PM** (monitorización del redimiento):
 + **NLon**: Número de bluces que han tardado más del tiempo estipulado en ejecutar. ( es decir, aquellos procesos que toman más de 5% de tiempo estipulada para ejecutar).
 + **NLoop**: El número total de bucles desde la última vez que se mostró el mensaje PM. Normalmente es 1000 y permite calcular el porcentaje de bucles que se ejecutan lentamente, nunca debe superar el 15%.
 + **MaxT**: El tiempo máximo que algún bucle tomó desde el último mensaje PM. Esto debería estar cerca de 10.000 pero será hasta 6.000.000 mientras se arman los motores.
 + **PMT**: Este número aumenta cada vez que se recibe un bit de vida desde la estación base. 
 + **I2CErr, INAVErr, INSErr**: el número de errores I2C, INAV e INS desde el último mensaje PM. Algunos errores I2C pueden indicar problemas en el bus I2C. 











