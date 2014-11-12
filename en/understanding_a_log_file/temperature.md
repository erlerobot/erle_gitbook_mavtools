# Temperature

Temperature is recorded from several sensors. For now only the BARO data contains value it:

```
1969-12-31 16:00:54.22: BARO {TimeMS : 871035, Alt : 0.167090296745, Press : 101289.78125, Temp : 25.56, CRt : -0.108711436391}
1969-12-31 16:00:54.24: BARO {TimeMS : 871135, Alt : 0.136959254742, Press : 101290.117188, Temp : 25.56, CRt : -0.0102719571441}
1969-12-31 16:00:54.26: BARO {TimeMS : 871235, Alt : 0.128741711378, Press : 101290.226562, Temp : 25.57, CRt : 0.102719441056}
1969-12-31 16:00:54.28: BARO {TimeMS : 871335, Alt : 0.027391852811, Press : 101291.398438, Temp : 25.56, CRt : 0.158359155059}
```

The field `Temp` provides information about the temperature acquired form the barometer in Celsius (º C).

We can graph these values with something like:
```
mavgraph.py 5.BIN "BARO.Temp"
```
![](../erleimg/temperature.png)

