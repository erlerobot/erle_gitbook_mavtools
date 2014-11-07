#LOITER

Loiter automatically attempts to maintain the current location, heading and altitude. The pilot may fly the copter in Loiter mode as if it were in manual. Releasing the sticks will continue to hold position.

Good GPS position, **low magnetic interference** on the compass and **low vibrations** are all important in achieving good loiter performance.

Loiter mode incorporates the altitude controller from AltHold mode.  Details for tuning AltHold are on [this page](altitude_hold.md).

##Controls
The pilot can control the copter’s position with the control sticks. In AC3.1 (and above) you may arm in Loiter mode but only once the GPS has 3D lock and the **HDOP has dropped to 2.0 or lower**.

- Horizontal location can be adjusted with the Roll and Pitch control sticks with the default maximum horizontal speed being 5m/s.  When the pilot releases the sticks the copter will slow to a stop.
- Altitude can be controlled with the Throttle control stick just as in [AltHold mode](altitude_hold.md).
- The heading can be set with the Yaw control stick

##Tunig

The maximum horizontal speed of the copter during loiter mode can be adjusted with the Loiter Speed (**WPNAV_LOIT_SPEED**) parameter. The value is expressed in cm/s so 500 = 5m/s.  The maximum acceleration during Loiter mode is always 1/2 of the Loiter speed.

The Loiter PID’s P value is used to convert the horizontal position error (i.e difference between the desired position and the actual position) to a desired speed towards the target position.  **It is generally not required to adjust this**. 

The Rate Loiter PID values are used to convert the desired speed towards the target to a desired acceleration.  The resulting desired acceleration becomes a lean angle which is then passed to the same angular controller used by [Stabilize mode](stabilization.md).  **It is generally not required to adjust this**.

##Verifying Loiter performance with dataflash logs

Viewing the loiter’s horizontal performance is best done by downloading a dataflash log from your flight, graph the NTUN message’s DesVelX vs VelX and DesVelY vs VelY.  In a good performing copter the actual velocities will track the desired velocities as shown below.  X = latitude (so positive = moving North, negative = South), Y = longitude (positive = East, negative = West).

```
mavgraph.py $LOITER1.BIN "NTUN.DVelX" "NTUN.VelX" --flightmode=apm
```

![velX](../erleimg/LOITER/loiterX.png)

```
mavgraph.py $LOITER1.BIN "NTUN.DVelY" "NTUN.VelY" --flightmode=apm
```

![velY](../erleimg/LOITER/loiterY.png)

Checking altitude hold performance is the same as for [AltHold mode](altitude_hold.md).

## Common problems

As mentioned above, Loiter mode incorporates the altitude controller from [AltHold mode](altitude_hold.md).

- The vehicle takes off in the wrong direction as soon as loiter is engaged.  The cause is the same as #1 except that the compass error is greater than 90deg.  Please try the suggestions above to resolve this.
- The vehicle is loitering normally and then suddenly takes off in the wrong direction.  This is generally caused by a GPS Glitch.  There is no 100% reliable protection against these which means the pilot should always be ready to take-over manual control.  Beyond that ensuring a good GPS HDOP before take-off is always good and it may help to reduce the GPSGLITCH_RADIUS and/or GPSGLITCH_ACCEL parameters to tighten up on the glitch detection.
