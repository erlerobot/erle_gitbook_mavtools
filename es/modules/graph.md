# Graph

El módulo de representación gráfica de datos en tiempo real del UAV. Es útil para la búsqueda de patrones de variación temporal.

Después de cargar el móduclo, se pueden añadir nuevas gráficas: 

```
graph add dataname
```

Varias variables pueden ser mostradas en la misma gráfica. Usa `:2` para especificar usar el eje vertical derecho.

```
graph add VFR_HUD.alt VFR_HUD.airspeed:2
```

O incluso funciones matemáticas:
```
graph add "(VFR_HUD.alt/1000.0)+5"
```