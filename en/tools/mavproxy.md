# MAVProxy

####reboot
Reboots the APM.

####setup
Goes into the setup (CLI) mode of the APM.

####rc
Override a RC (input) channel. This value remains in effect until a value of -1 is set. Uses the form of rc chan value. Use all to set a global value for all RC channels.

```
rc 1 1000
rc all -1
```

####time
Displays the current on the autopilot, if supported. The time in the brackets is the ground station time.

####link
Displays the telemetry link(s) status.

####script
Runs a text file containing MAVProxy commands, much like the startup scripts.

####status
Shows the latest packets received from the autopilot. Useful for reading the state of the UAV.
