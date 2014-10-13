# Installing MAVProxy
Mavproxy is a tool we will use to analyse and control the flight logs. You will need to have Python 2.7 installed first. MAVProxy is hosted on PyPi and the installation packages can be found there: [MAVProxy](https://pypi.python.org/pypi/MAVProxy) and [MAVLink](https://pypi.python.org/pypi/pymavlink).

##Linux
Linux users can use the PyPi program to get the needed packages:

```
sudo apt-get install python-pip
```

####Installing necessary packages

Some modules will be, probably, necessary.

```
sudo apt-get install python-opencv
sudo apt-get install python-wxgtk2.8
sudo apt-get install python-matplotlib
sudo apt-get install python-numpy
sudo apt-get install python-serial
sudo apt-get install python-pil
sudo apt-get install libwxgtk2.8-dev
```

####Installing MAVProxy
Download and install MAVProxy. Note a sudo may be required in some circumstances if the install generates errors.

```
sudo pip install MAVProxy
```

##MACOS

####Macports
The first thing we have to do It's to install MACPorts, this project is an open-source community initiative to design an easy-to-use system for compiling, installing, and upgrading either command-line, X11 or Aqua based open-source software on the OS X operating system. [Here](https://guide.macports.org/chunked/installing.macports.html) you can find all the necessary information to install `macports`.

####Installing necessary packages
Some modules will be necessary.

````
sudo port install py27-serial
sudo port install py27-matplotlib
sudo port install py27-wxpython-2.8
sudo port install opencv
sudo port install py27-numpy
sudo port install py27-parsing
sudo port install py27-pil
```

####Installing pip
```
sudo port install py27-pip
```
####Installing MAVProxy
Download and install MAVProxy. Note a sudo may be required in some circumstances if the install generates errors.

`sudo pip-2.7 install MAVProxy`
