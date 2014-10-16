# Glossary

Aquí nos juntamos todos los comandos introducidos a través de la GitBook:

*Representa la latitud y longitud del GPS*
```bash
mavgraph.py 30.BIN "GPS.Lat" "GPS.Lng" --flightmode=apm
```
*Representa el pitch y el pitch deseado*
```bash
mavgraph.py 30.BIN "ATT.DesPitch" "ATT.Pitch" --flightmode=apm
```
*Representa el roll y el roll deseado*
```bash
mavgraph.py 30.BIN "ATT.DesRoll" "ATT.Roll" --flightmode=apm
```
*Representa los valores en burto de los acelerometros*
```bash
mavgraph.py 30.BIN "IMU.AccX" "IMU.AccY" "IMU.AccZ" --flightmode=apm
```
Altitude measurements unstable:
*Representa el valor en bruto de la altura (CTUN.BarAlt), altura estimada (CTUN.Alt) y altura deseada (CTUN.DAlt)*
```bash
mavgraph.py 30.BIN "CTUN.BarAlt" "CTUN.Alt" "CTUN.DAlt" --flightmode=apm
```