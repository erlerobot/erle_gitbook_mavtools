#Modos de vuelo

Hay 14 modos de vuelo disponibles en APM:Copter, 10 de ellos son los usados habitualmente. Tu puedes condigurarlos haciendo lo siguiente:

+ Enciendo tu radio control
+ Conecta tu placa a *Mision Planner* o a *QGroundControl*
+ Ve a la pantalla de modos de vuelo
+ Comprueba que puedes visualizar cambios en el canal 5. Resaltará en verde la barra actual de posición.
+ Puedes configurar hasta 6 modos de vuelo diferentes con el mando.
+ Guarda los cambios antes de salir.

#Modos
+ **Stabilize**: El modo *Stabilize* permite volar el vehículo manualmente, pero estabiliza automáticamente el *pitch* y *roll*.
+ **Altitude hold mode**: En el modo bloque de altitud, el vehículo mantiene una antura, permitiendo controlar normalmente el *roll*, *pitch*, and *yaw*
+ **Loiter**: El modo *Loiter* mantiene la posición actual. El piloto puedo volar el vehículo como si estuviera en manual. Pero cuando suelta los stick continuará manteniendo la posición.
+ **RTL Mode**: En el modo retorno al inicio, el vehículo navega desde su posicón actual hasta la posición de inicio. El comportamiento de *RTL* puede ser controlado con diferentes parámetros ajustables.
+ **Auto Mode**: En el modo automático una misión pre-programada y almacenada en el autopiloto puede ser llevada a cabo sin intervención de usuario.
+ **Acro**: El modo *Acro* utiliza los controles del radio mando para regular la velocidad angular del veículo. Soltando los *sticks* del mando y mantiene la altitud actual. El modo *Acro* es útil para realizar acrobacias como *flips* o *rolls*.
+ **Sport**: El modo *Sport* esta diseñado para ser útil cuando se realizan vuelos con *FPV* ya que puede mantener un ángulo en particular.
+ **Drift**: El modo *Drift* permite al usuario volvar un multi-coptero como si de un avión se tratase.
+ **Guided Mode**: El modo *Guided* es capaz de seguir dinámicamente un objetivo enviando su localazión por telemetría o una estación de control de tierra.
+ **Circle Mode**: El modo *Circle* permite orbitar alrededor de un punto interesante.
+ **Position Mode**: El modo *Position* es parecido al modo *loiter* pero con el control manual del acelerador. Esto significa que, en el modo posición, el vehículo mantiene la posición pero el piloto debe controlar el acelerador manualmente.
+ **Land Mode**: El modo aterrizaje permite llevar el vehículo lentamente a tierra.
+ **Follow Me Mode**:hace posible que el vehículo te siga cuando te mueves, usando la telemetría de radio o una estación de control de tierra. Como por ejemplo: Mision Planner, APM Planner or DroidPlanner.
+ **Simple and Super Simple Modes**: El modo *Simple* o "Super simple" es una combinación de varios modos de vuelo: *Stabilize*, *Sport*, *Drift* and *Land*. Permite al piloto controlar el movimiento del vehículo desde el punto de vista del piloto.


####Dependencia del GPS
Requiere tener señal GPS para despegar:

+ Loiter (& OF_loiter)
+ RTL (Return-to-Launch)
+ Auto
+ Guided
+ Drift
+ Position
+ Follow Me
+ Circle

No requieren señal GPS:

+ Stabilize
+ Alt Hold
+ Acro
+ Sport
+ Land
