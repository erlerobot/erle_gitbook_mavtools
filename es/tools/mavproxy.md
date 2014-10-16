# MAVProxy

MAVProxy es unà estación de control en tierra con total funcionalidad para el UAV. La intención es que sea minimalista, portable y extensible para cualquier UAV que soporte el protocolo MAVLink (como el APM). 

##Características
+ Es una aplicación basada en línea de comandos en consola. Hay algunos *plugins* que se incluyen en MAVProxy que proporcionan un GUI.
+ Puedes ser ejecutada en red y a tráves de varios computadores 
+ Es portable; debería funcionar en cualquier sistema POSIX con Python, pyserial y llamadas al sistema select(), lo que significa Linux, OS X, Windows, y otros.
+ El diseño ligero permite ejecutarlo en pequeños ordenadores con facilidad.
+ Es compatible con módulos de carga dinámica, y cuenta con módulos de apoyo a la consola, mapas móviles, joysticks, rastreadores de antena, etc
+ Autocompletado con tabulador