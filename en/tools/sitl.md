# SITL

The SITL (Software In The Loop) simulator allows you to run APM  without any hardware. It is a build of the autopilot code using an ordinary C++ compiler and giving you a native executable that allows you to test the behaviour of the code without hardware.

![](http://dev.ardupilot.com/wp-content/uploads/sites/6/2013/04/SITL_Linux.png)

### Installation
Refer to the [APM wiki](http://dev.ardupilot.com/wiki/setting-up-sitl-on-linux/) for installation instructions.

### Once installed compile and lunch the simulator
```bash
sim_vehicle.sh -w
```
