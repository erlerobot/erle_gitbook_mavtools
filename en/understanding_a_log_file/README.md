# Understanding a log file

There are two ways to record your flight data with ArduCopter. With some exceptions, the two methods record very similar data but in different ways:

+ **Dataflash logs** use the BeagleBoard dataflash memory, which you can download after the flight. On ArduPlane and ArduRover dataflash logs are created soon after start-up. On *ArduCopter they are created after you first arm the copter*.
+ **Telemetry logs** (also known as “tlogs”) are recorded by the MAVProxy (or other ground station: Mision Planner, QGroundControl, etc) when you connect your APM to your computer via telemetry link. You can find the details here.

##Dataflash logs

###Message details (APM:Copter specific)
+ **ATT** (attitude information)
 + DesRoll: the pilot’s desired roll angle in centi-degrees (roll left is negative, right is positive)
  + Roll: the vehicle’s actual roll in centi-degrees (roll left is negative, right is positive)
  + DesPitch: the pilot’s desired pitch angle in centi-degrees (pitch forward is negative, pitch back is positive)
  + Pitch: the vehicle’s actual pitch angle in centi-degrees (roll left is negative, right is positive)
  + DesYaw: the desired heading in centi-degrees
  + Yaw: the vehicles actual heading in centi-degrees with 0 = north
+ **IMU** (accelerometer and gyro information):
  + GyrX, GyrY, GyrZ: the raw gyro rotation rates in degrees/second
  + AccX, AccY, AccZ: the raw accelerometer values in m/s/s
+ **GPS**
 + Lat: Lattitude according to the GPS
 + Lng: Longitude according to the GPS
+ **RCOUT** (pwm output to individual RC outputs): RC1, RC2, etc : pwm command sent from flight controller to the esc/motor/RC output
+ **CTUN** (throttle and altitude information):
 + Alt: the command’s altitude in meters
 + BarAlt: the altitude above ground according to the barometer
 + DAlt: the desired altitude while in AltHold, Loiter, RTL or Auto flight modes
+ **BARO** (barometer information):
 + Alt (0.0602620765567) ?
 + Press : (101291.015625) ?
 + Temp : (25.57) Temperature in Celsius (º C).
 + CRt : (0.0213998798281) ?
+ **PM** (performance monitoring):
 + NLon: number of long running main loops (i.e. loops that take more than 5% longer than the 10ms they should)
 + NLoop: the total number of loops since the last PM message was displayed. Normally 1000 and allows you to calculate the percentage of slow running loops which should never be higher than 15%.
 + MaxT: the maximum time that any loop took since the last PM message. This should be close to 10,000 but will be up to 6,000,000 during the interval where the motors are armed
 + PMT: a number that increments each time a heart beat is received from the ground station
 + I2CErr, INAVErr, INSErr: the number of I2C, INAV and INS errors since the last PM message. Any I2C errors may indicate a problem on the I2C bus which may in turn slow down the main loop and cause performance problems.









