# Barometer-pitch and roll linkage

Sometimes the altitude lost 1m ~ 2m when the copter levels out after a high speed forward flight. This is caused by an aerodynamic effect which leads to a momentary low pressure bubble forming on the top of the copter where the flight controller is mounted which leads the altitude hold controller to believe it is climbing so it responds by descending. 

In the following graph we can observe this fact. The graph shows the altitude, BarAlt (barometer altitude), DAlt (desired altitude) and Alt (inertial nav altitude estimate).

![alt_barometerx](../erleimg/alt_barometer.png)

The next graph shows the radio control input. The blue and yellow lines represent the throttle and the yaw (the joystick on the left). The green and red lines represent the roll and pitch (the joystick on the right).

![rc_barometer](../erleimg/rc_barometer.png)

Look at the changes in the red line when the value is close to 2000 (or 1000), it means that we produce a high speed forward flight or when we show the green line close to 2000 ( or 1000), it means that we produce a high speed flight to one side. If we observe this instants in the altitude graph we see that the barometers changes the value 1 or 2 meters.

**There is no cure for this behaviour at the moment although increasing the INAV_TC_Z parameter to 7 (default is 5) reduces the effect but increases the copter climbing as soon as altitude hold is engaged.**


The parameter `INAV_TC_Z` (Vertical Time Constant) is the time constant for barometer and accelerometer mixing. TC decreases barometers impact on altitude estimate. (Range: 0 10, Increment: 0.1)
