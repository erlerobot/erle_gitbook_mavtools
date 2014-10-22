# MAVProxy

MAVProxy es unà estación de control en tierra con total funcionalidad para el UAV. La intención es que sea minimalista, portable y extensible para cualquier UAV que soporte el protocolo MAVLink (como el APM). 

##Características
+ Es una aplicación basada en línea de comandos en consola. Hay algunos *plugins* que se incluyen en MAVProxy que proporcionan un GUI.
+ Puedes ser ejecutada en red y a tráves de varios computadores 
+ Es portable; debería funcionar en cualquier sistema POSIX con Python, pyserial y llamadas al sistema select(), lo que significa Linux, OS X, Windows, y otros.
+ El diseño ligero permite ejecutarlo en pequeños ordenadores con facilidad.
+ Es compatible con módulos de carga dinámica, y cuenta con módulos de apoyo a la consola, mapas móviles, joysticks, rastreadores de antena, etc
+ Autocompletado con tabulador


Uso:
```bash
mavproxy.py [options]
```
Opciones:
```bash
  -h, --help            show this help message and exit
  --master=DEVICE[,BAUD]
                        MAVLink master port and optional baud rate
  --out=DEVICE[,BAUD]   MAVLink output port and optional baud rate
  --baudrate=BAUDRATE   default serial baud rate
  --sitl=SITL           SITL output port
  --streamrate=STREAMRATE
                        MAVLink stream rate
  --source-system=SOURCE_SYSTEM
                        MAVLink source system for this GCS
  --target-system=TARGET_SYSTEM
                        MAVLink target master system
  --target-component=TARGET_COMPONENT
                        MAVLink target master component
  --logfile=LOGFILE     MAVLink master logfile
  -a, --append-log      Append to log files
  --quadcopter          use quadcopter controls
  --setup               start in setup mode
  --nodtr               disable DTR drop on close
  --show-errors         show MAVLink error packets
  --speech              use text to speach
  --aircraft=AIRCRAFT   aircraft name
  --cmd=CMD             initial commands
  --console             use GUI console
  --map                 load map module
  --load-module=LOAD_MODULE
                        Load the specified module. Can be used multiple times,
                        or with a comma separated list
  --mav09               Use MAVLink protocol 0.9
  --auto-protocol       Auto detect MAVLink protocol version
  --nowait              don't wait for HEARTBEAT on startup
  -c, --continue        continue logs
  --dialect=DIALECT     MAVLink dialect
  --rtscts              enable hardware RTS/CTS flow control
  --mission=MISSION     mission name
```