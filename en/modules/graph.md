# Graph

A module to plot (graph) data in realtime from the UAV. It is useful for looking for time-varying patterns in the data

After loading, new plots can be created by:

```
graph add dataname
```

Multiple items can be added at one. Use the :2 to specify using the right vertical axis.

```
graph add VFR_HUD.alt VFR_HUD.airspeed:2
```

Aribary mathematical functions can alse be used.
```
graph add "(VFR_HUD.alt/1000.0)+5"
```