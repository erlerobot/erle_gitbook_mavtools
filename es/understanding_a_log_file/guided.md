# GUIDED MODE

El modo guiado es una de las posibilidades de APM:Copter para guiar dinámicamente al vehículo a una localización de forma inalámbrica a través de telemetría y una estación de control de tierra. Esta pagina proporciona algo de información.

El modo guiado no es un modo tradicional de vuelo que pueda ser asignado a un *switch* del radio mando como otros modos de vuelo. El modo guiado se utiliza junto con una estación de control en tierra (como Mision Planner, DroidPlanner, etc) y telemetría por radio. Este modo permite interactuar con el vehículo para desplazarlo a una localización concreto haciendo click sobre el mapa que proporciona la estación de control en tierra. Una vez que la localización es alcanzada, el vehículo mantendrá la posición, esperando al siguiente objetivo. El modo ** Follow me ** también utiliza el modo de guiado para hacer que el copter siga al piloto.

#### Instrucciones

- Configura el vehículo y establece una conexión MAVLink a traves de telemetría wifi entre tu vehículo y tu ordenador o smartphone.
- En tu ordenador o smartphone comprueba que todo este funcionando correctamente y que tengas el bloqueo de GPS.
- Despega el vehículo, y en una altura razonable cambia al modo Loiter.
- En el mapa que proporcione tu estación de control introduce un punto de destino.
- El vehículo debe volar hasta la localización destino y esperará en ese lugar hasta que se introduzca otra localización o se cambie de modo.
