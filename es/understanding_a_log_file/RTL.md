# Vuelta al punto de partida (RTL)

En el modo vuelta al punto de partida, el vehículo navega desde su posicion actual hasta aterrizar en la posición de partida. El comportamiento de el modo RTL puede ser controlado por varios parámetros ajustables. Esta página descibre como usar y custimozar el modo RTL.

Cuando el modo RTL esta selecionado el vehículo volverá a su posición inicial. El vehículo primero sube hasta la altura definida en RTL_ALT antes de iniciar la navegación o mantiene la altitud si esta es mayor que la definida en el parámetro **RTL_ALT*. El valor por defecto de **RTL_ALT** es 15 meters.

RTL depende su movimiento de GPS, esencialmente que el bloqueo del GPS este activo antes de utilizar este modo de vuelo. Antes de armar, asegurate de que el LED azul del GPS+Brújula esta parpadeando. Para un GPS sin brújula, el LED azul estará fijo cuando el bloqueo del GPS esté activo.

RTL mandará al vehículo volver a la posición de partida, significa volver a la localización donde fue armado. **Por lo tanto**, la posición inicial donde el vehículo despegó se supone siempre libre se obstáculos y alejada de personas. Para APM:Copter si se dispone del bloqueo del GPS y luego armas el vehículo, la posición de partida será donde fue armado. Esto significa que si ejecutas RTL en APM:Copter, volverá a la localización donde fue armado.

**Cuidado**: En el modo RTL el controlador de vuelo utiliza un barómetro que mide la presión del aire para determinar la altitud y si la presión del aire esá cambiando en tu zona de vuelo, el vehículo seguirá el cambio de presión en lugar de la altitud real (a menos que se disponga de un sonar instalado,  habilitado y que esté a menos de 6 metros del suelo).

## Opciones

- *RTL_ALT*: La altura mínima que el vehículo alcanzará antes de volver al inicio.
 - El valor a 0 vuelve en la altura actual.
 - La altura de retorno puede fijarse desde 1 a 8000 centímetros.
 - La altura de retorno por defecto es 15 metros (1500).
- *RTL_ALT_FINAL*: La altura a la que el vehículo se moverá al final de la etapa *vuelta al inicio* o después de completar la misión.
 - El valor a cero indica que el vehículo aterrizará automáticamente.
 - El valor final de la altura de retorno se puede ajustar entre 0 a 1000 centímetros.
- *RTL_LOIT_TIME*: Tiempo en milisegundo que mantendrá la posición antes de iniciar el descenso.
 - El tiempo que mantendrá la posición puede ajustarse desde 0 a 60 milisegundos.
- *WP_YAW_BEHAVIOR*: Ajusta como el autopiloto controla el *Yaw* duranto una misión y RTL.
 - 0 = Nunca cambia el Yaw.
 - 1 = Se enfreta al siguiente *waypoint* incluyendo hacia el punto de partida en RTL.
 - 2 = Se enfrenta al siguiente *Waypoint* excepto en RTL (por ejemplo durante RTL el vehículo mantendrá su última orientación)
- *LAND_SPEED*: La velocidad de descenso para la fase final de aterrizaje en centímetros por segundo.
 - La velocidad de descenso puede ajustarse entre 20 y 200 centímetros por segundo.

## Notas

- Otros parámetros de navefación pueden influir sobre el modo RTL:
 - WPNAV_ACCEL
 - WPNAV_LOITER_SPEED
 - WPNAV_SPEED_DN
 - WPNAV_SPEED_UP
- Para usar RTL, el bloqueo del GPS tiene que estar activo antes de armar y despegar para establecer la punto de partida.
- Ten en cuenta que el LED del módulo GPS UBLOX esta apagado mientras esta adquiriendo satélites y parpadeando cuando tiene satélites.
- Aterrizar y re-armar el vehículo reseteará el punto de partida, esto es una gran característica para volar en campos de aviación.
- Si obtiene el bloqueo del GPS mientras esta volando, tu punto de partida será donde ha cogido el bloqueo el GPS, no el punto de partida real.
- Si ajustas el parámetro *ALT_HOLD_RTL* a un número distinto de 0, irá y mantendrá la altitud mientras retorna.
- RTL usa el parámetro *waypoint_speed* para determinar como de rápido navega.
- Una vez que el vehículo vuelve al punto de partida, el vehículo entra en modo Loiter durante un tiempo y luego aterriza.
- Para prevenir un aterrizaje automático, simplemente cambia de modo con el radio mando para volver a obtener el control del vuelo.
- El *stick* del Throttle controla la altitud mientras vuelve o esta en el modo loiter sobre el punto de partida, no directamente sobre los motores.