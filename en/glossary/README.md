# Glossary

Here we put together all the commands introduced through the GitBook:

*graph GPS Latitude and Longitude*
```bash
mavgraph.py 30.BIN "GPS.Lat" "GPS.Lng" --flightmode=apm
```
*graph pitch and desired pitch*
```bash
mavgraph.py 30.BIN "ATT.DesPitch" "ATT.Pitch" --flightmode=apm
```
*graph roll and desired roll*
```bash
mavgraph.py 30.BIN "ATT.DesRoll" "ATT.Roll" --flightmode=apm
```
*graph raw accelermeters values*
```bash
mavgraph.py 30.BIN "IMU.AccX" "IMU.AccY" "IMU.AccZ" --flightmode=apm
```

Altitude measurements unstable:
*graph raw altitude (CTUN.BarAlt), estimated (CTUN.Alt) and desired one (CTUN.DAlt)*
```bash
mavgraph.py 30.BIN "CTUN.BarAlt" "CTUN.Alt" "CTUN.DAlt" --flightmode=apm
```

GPS
mavgraph.py 30.BIN "GPS.Lat" "GPS.Lng" --flightmode=apm
