# Map

Una pantalla que contiene un mapa con la información de la posición actual del UAV, waypoints y *geofence*.

Los mapas son descargados y almacenados en caché en el disco local del usuario automáticamente. El módulo utilizará estos archivos si no encuentra una conexíon a Internet.

Para visualizar los *waypoints* y *geofence*, se pueden usar los comandos `wp list` y `fence list`.

La edición de *waypoints* permite clicando en el botón derecho selecionar *waypoint* y luego clicando sobre el derecho moverlos.

Para dibujar un conjuntos de *waypoints* uitliza `wp draw`, clicando en el botón derecho para los *waypoints* deseados:

Cuando finalices, utiliza `wp loop` para conectar el último *waypoint* con el primero, creado un bucle.

Para cargar el módulo:

```
module load map
```

Usa la tecla "g" para especificar una posición para mover el mapa.

![map](../erleimg/modules/map.png)
