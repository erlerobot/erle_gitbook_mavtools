# GUIDED MODE

Guided mode is a capability of APM:Copter to dynamically guide the copter to a target location wirelessly using a telemetry radio module and ground station application. This page provides instructions for using guided mode.

Guided mode is not a traditional flight mode that would be assigned to a mode switch like other flight modes. The guided mode capability is enabled using a ground station application (such as Mission Planner) and telemetry radio. This capability allows you to interactively command the copter to travel to a target location by clicking on a point on the Ground Station Flight Data map. Once the location is reached, the copter will hover at that location, waiting for the next target. **Follow Me** mode also uses Guided Mode to make the copter follow the pilot around the field.

#### Instructions

- Set up your copter at the field and establish a MAVLink connection over wireless telemetry between your copter and your laptop.
- On your laptop make sure that it’s working and that you have a GPS lock.
- Take off in Stabilize mode and once at a reasonable altitude, switch to Loiter.
- In the Ground Station Flight Data screen map, try right-clicking on a nearby spot.
- The vehicle should fly to the target location and wait there until you enter another location or switch to another mode.


**Note**: There’s no need to set up one of your flight modes as “Guided”

