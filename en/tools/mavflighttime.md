# MAVFlighttime
Prints out the total time spent in the air. Note that a threshold of 3m/s defines the difference between air time and ground time. This can be changed by the --groundspeed= argument.

Usage:

```
mavflighttime.py 1.BIN
```

You can see a summary of your flights:

```
In air at Thu Oct  9 16:56:51 2014 (percent 27% groundspeed 3.6)
On ground at Thu Oct  9 16:56:52 2014 (percent 27.5% groundspeed 2.3  time=1.0 seconds)
In air at Thu Oct  9 17:02:41 2014 (percent 85% groundspeed 3.1)
On ground at Thu Oct  9 17:02:41 2014 (percent 85.0% groundspeed 2.3  time=0.0 seconds)
In air at Thu Oct  9 17:03:22 2014 (percent 95% groundspeed 3.0)
On ground at Thu Oct  9 17:03:22 2014 (percent 94.9% groundspeed 2.6  time=0.0 seconds)
Flight time : 0:01
Total time in air: 0:01
Total distance trevelled: 258.3 meters
```
