# Instalando MACProxy
MAVProxy es una herramienta utilizada para el análisis y el control de los logs de vuelo. Necesitas tener Python 2.7 instalado. MAVProxy esta alojado en PyPi y los paquetes de inslación se pueden encontrar en : [MAVProxy](https://pypi.python.org/pypi/MAVProxy) y [MAVLink](https://pypi.python.org/pypi/pymavlink).

##Linux
Los usuarios de Linux pueden usar PyPi para obtener los paquetes necesarios
Linux users can use the PyPi program to get the needed packages:

```
sudo apt-get install python-pip
```

####Instalando los paquetes necesarios

Algunos modulos que son necesarios:

```
sudo apt-get install python-opencv
sudo apt-get install python-wxgtk2.8
sudo apt-get install python-matplotlib
sudo apt-get install python-numpy
sudo apt-get install python-serial
sudo apt-get install python-pil
sudo apt-get install libwxgtk2.8-dev
```

####Instalando MAVProxy
Descarga e instala MAVProxy. Es posible que requiera permisos de `sudo`.

```
sudo pip install MAVProxy
```

## Mac OS

####[Macports](https://guide.macports.org)
Lo primero es instalar  [MACPorts](https://guide.macports.org), este proyecto es una iniciativa de la comunidad open-source para desarrollar un sistema sencilla para la compilación, instalación y actualización de paquetes para la línea de comandos, X11 o Aqua basatado en el sotfware open-source disponible para MACOS. [Aquí](https://guide.macports.org/chunked/installing.macports.html) puedes encontrar toda la información necesaria para instalar `macports`.

####Instalando los paquetes necesarios
Algunos modulos que son necesarios:

````
sudo port install py27-serial
sudo port install py27-matplotlib
sudo port install py27-wxpython-2.8
sudo port install opencv
sudo port install py27-numpy
sudo port install py27-parsing
sudo port install py27-pil
```

####Instalando pip
MAVProxy esta alojado en PyPi. Puedes usar `pip` para instalar MAVProxy.

```
sudo port install py27-pip
```
####Instalando MAVProxy
Descarga e instala MAVProxy. Es posible que requiera permisos de `sudo`.

`sudo pip-2.7 install MAVProxy`
