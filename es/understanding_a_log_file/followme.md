# Follow Me Mode

El **modo follow me** hace posible tener al vehículo siguiendote, usando la telemetría y una estación de control en tierra. Lo más sencillo es utilizar un smartphone o tablet como estación de control en tierra. El modo de seguimiento de APM:Copter utiliza los *waypoints* de manera dinámica y comandos de MAVLink.

#### Que se necesita:
 - APM::copter con telemetría
 - Un ordenador o un smartphone/tablet
 - Señal GPS en el vehículo y en la estación de control en tierra

 #### Instruciones
- Configura APM:Copter en tierra y establece una conexión MAVLink a través de la telemetría.
- Comprueba que tengas la señal de GPS bloqueada
- Despega y cambia al modo de vuelo **Loiter** (con la suficiente altura para evitar que cuando te siga te pueda producir algún daño ).
- En el mapa de la estación de control de tierra intenta poner un punto para el seguimiento en modo **GUIDED**. Si esto te funciona estás listo para utilizar el modo de seguimiento..
 - Como se ha mencionado anteriormente, sube lo suficiente el vehículo para evitar posible daños
 - Esta es una gran capacidad, pero la seguridad es muy importante en este modo sobre todo si las hélices están al descubierto.

**Atención**: Como otros modos de vuelo donde el autopiloto controla la altitud (Loiter, AltHold, etc), el barómetro se utiliza para calcular la altura, esto significa que la altitud puede modificarse con el paso del tiempo y el vehñiculo seguira el cambio de presión en lugar de la altura real sobre el suelo.

 
