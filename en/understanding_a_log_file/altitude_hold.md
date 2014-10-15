# Altitude hold

In **altitude hold mode**, the copter maintains a consistent altitude while allowing roll, pitch, and yaw to be controlled normally. This page contains important information about using and tuning alt hold.

When altitude **hold mode** (aka **AltHold**) is selected, the throttle is automatically controlled to maintain the current altitude. Roll, Pitch and yaw operate the same as in *Stabilize* mode meaning that the pilot directly controls the roll and pitch lean angles and the heading.

Automatic altitude hold is a feature of many other flight modes (Loiter, Sport, etc) so the information here pertains to those modes as well.

**Note**: The flight controller uses a barometer which measures air pressure as the primary means for determining altitude (“Pressure Altitude”) and if the air pressure is changing in your flight area due to extreme weather, the copter will follow the air pressure change rather than actual altitude (unless you are within 20 feet of the ground and have SONAR installed and enabled). Below 26 feet, SONAR (if enabled) will automatically provide even more accurate altitude maintenance.

##Controls
The pilot can control the climb or descent rate of the vehicle with the throttle stick.

+ If the throttle stick is in the middle (40% ~ 60%) the vehicle will maintain the current altitude.

## Verifying AltHold performance with dataflash logs

Viewing the altitude hold performance is best done by downloading a dataflash log from your flight, then open it with **mavgraph** and graph the barometer altitude, desired altitude and inertial navigation based altitude estimate.  This data is found in slight different columns depending upon the version and board.


APM running AC3.2 or Pixhawk running AC3.1 or AC3.2: CTUN’s BarAlt (baro alt), DAlt (desired alt) and Alt (inertial nav alt estimate)

The three should track well as shown below.

![roll](../erleimg/ALT_HOLD/ALT_HOLD.png)
