# Follow Me Mode

The **follow me mode** makes it possible for you to have your copter follow you as you move, using a telemetry radio and a ground station. it’s easiest to use a phone or tablet as your Follow Me ground station. Follow Me mode uses the APM:Copter dynamic waypoint feature and MAVLink telemetry commands.

#### What you’ll need:
 - An APM:Copter with telemetry
 - A laptop or a smartphone
 - GPS signal in your Ground Station.

 #### Instructions
- Set up your APM:Copter at the field and establish a MAVLink connection over wireless telemetry
- Set one of your flight modes to “Loiter”
- Ensure that your GPS device is connected.
- Take off, and once in the air switch to Loiter. (Sufficient altitude to ensure that while it is following you it isn’t attacking you might be a good idea).
- In the Ground Sattion Flight Data screen try to click on a nearby spot. If this works, you’re ready to try Follow Me mode.
 - If you have set the altitude to 5 feet it might be a good idea to see if you can out run it.
 - As mentioned before, sufficient altitude to prevent injury is useful.
 - Seriously this is a great capability, but safety is really important when using Follow Me mode especially with an open bladed Multicopter.

**Warning**: Like all other modes in which the autopilot is responsible for altitude hold (Loiter, AltHold), the barometer is used in the altitude calculation meaning that it can drift over time and the copter will follow the air pressure change rather than actual altitude above ground.



