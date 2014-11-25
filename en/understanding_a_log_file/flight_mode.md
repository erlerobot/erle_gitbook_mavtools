# Flight mode

There are 14 flight modes available in APM:Copter, 10 of which are regularly used.  You can set these up by doing the following:

+ Turn on your RC transmitter
+ Connect your board to Mission Planner or QGoundControl
+ Go to Flight Modes screen
+ Note as you move your transmitter’s flight mode switch (channel 5) the green highlight bar will move to a different position.
+ Use the drop-down on each line to select the flight mode for that switch position ensuring that at least one switch position is left assigned to Stabilize
+ When finished press the “Save Modes” button.

####Modes
+ **Stabilize**: Stabilize mode allows you to fly your vehicle manually, but self-levels the roll and pitch axis.
+ **Altitude hold mode**: In altitude hold mode, the copter maintains a consistent altitude while allowing roll, pitch, and yaw to be controlled normally.
+ **Loiter**: Loiter automatically attempts to maintain the current location, heading and altitude. The pilot may fly the copter in Loiter mode as if it were in manual. Releasing the sticks will continue to hold position.
+ **RTL Mode**: In return to launch (RTL) mode, the copter navigates from its current position to hover above the home position. The behavior of RTL mode can be controlled by several adjustable parameters.
+ **Auto Mode**: In Auto mode the copter will follow a pre-programmed mission script stored in the autopilot which is made up of navigation commands (i.e. waypoints) and “do” commands (i.e. commands that do not affect the location of the copter including triggering a camera shutter).
+ **Acro**: Acro mode (Rate mode) uses the RC sticks to control the angular velocity of the copter. Release the sticks and the vehicle will maintain its current attitude and will not return to level. Acro mode is useful for aerobatics such as flips or rolls, or FPV when smooth and fast control is desired.
+ **Sport**: Sport Mode is also known as “rate controlled stabilize” plus Altitude Hold. It was designed to be useful for flying FPV and filming dolly shots or fly bys because you can set the vehicle at a particular angle and it will maintain that angle.
+ **Drift**: Drift Mode allows the user to fly a multi-copter as if it were a plane with built in automatic coordinated turns.
+ **Guided Mode**:Guided mode is a capability of APM:Copter to dynamically guide the copter to a target location wirelessly using a telemetry radio module and ground station application.
+ **Circle Mode**: Circle will orbit a point of interest with the nose of the vehicle pointed towards the center.
+ **Position Mode**: Position mode is the same as loiter mode, but with manual throttle control. This means that, in position mode, the copter maintains a consistent location and heading, while allowing the operator to control the throttle manually.
+ **Land Mode**: LAND mode attempts to bring the copter straight down.
+ **Follow Me Mode**: makes it possible for you to have your copter follow you as you move, using a telemetry radio and a ground station. Mission Planner for Windows laptops, APM Planner for OS X laptops, and DroidPlanner for Android devices currently support Follow Me; however, it’s easiest to use a phone or tablet as your Follow Me ground station.
+ **Simple and Super Simple Modes**: “Simple” and “Super Simple” modes are used in combination with the Stabilize, Sport, Drift and Land flight modes. They allow the pilot to control the movement of the copter from the pilot’s point of view regardless of which way the copter is facing.

####GPS Dependency

Requires GPS lock prior to takeoff:

+ [Loiter (& OF_loiter)](loiter.md)
+ [RTL (Return-to-Launch)](RTL.md)
+ [Auto](auto.md)
+ [Guided](guided.md)
+ [Drift]()
+ [Position](position.md)
+ [Follow Me](followme.md)
+ [Circle]()

Does not require GPS lock:

+ [Stabilize](Stabilization.md)
+ [Alt Hold](altitude_hold.md)
+ [Acro]()
+ [Sport]()
+ [Land](land.md)
