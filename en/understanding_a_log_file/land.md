# Land

LAND mode attempts to bring the copter straight down.

+ **Descends to 10m** (or until the sonar senses something below the copter) using the regular Altitude Hold controller which will descend at the speed held in the WPNAV_SPEED_DN parameter which can be modified
+ **Below 10m** the copter should descend at the rate specified in the LAND_SPEED parameter which defaults to 50cm/s.
+ Upon reaching the ground the copter will automatically shut-down the motors and disarm the copter if the pilot’s throttle is at minimum.

**NOTES**:
+ If the vehicle does not have GPS lock the horizontal control will be as in stabilize mode so the pilot can control the roll and pitch lean angle of the copter.
+ If the vehicle has GPS lock the landing controller will attempt to control it’s horizontal position but the pilot can adjust the target horizontal position just as in Loiter mode.

**Warning!**

In any Alt Hold based mode. If your copters operation becomes erratic when you are close to the ground or landing you probably have the fight controller situated such that it’s barometer (altimeter) is being affected by **the pressure created by the copters prop-wash against the ground**.
+ This is easily verified by looking at the Altimeter reading in your logs and seeing if it spikes or oscillates when near the ground.
+ If this is a problem, move the flight controller out of prop wash effect or shield it with an appropriately ventilated enclosure.
Success can be verified by flight test and by log results.
