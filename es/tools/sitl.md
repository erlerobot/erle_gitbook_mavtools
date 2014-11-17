# SITL

El simulador SITL permite ejecutar APM sin ningún tipo de hardware. El código del autopiloto se compila utilizando un compilar de C++ ordinario, de tal forma que se obtiene un ejecutable que le permite probar el comportamiento del código sin necesidad de hardware. 

![](http://dev.ardupilot.com/wp-content/uploads/sites/6/2013/04/SITL_Linux.png)

### Instalación en Ubuntu
Revise la [wiki de APM](http://dev.ardupilot.com/wiki/setting-up-sitl-on-linux/) para las instrucciones de instalación

#### Lanzando el simulador
```bash
sim_vehicle.sh -w
```

### Instalación en Mac OS
Instalar solo las herrameintas de línea de comando para OSX incluyendo GCC, a comtinuación instala los siguientes módulos en Python:
```bash
sudo easy_install pip
sudo pip install pexpect
sudo pip install pyserial
```
Instalando MAVLink y MAVProxy
```bash
sudo pip install pymavlink MAVProxy
```

---

** o instala MAVLink y MAVProxy desde los fuentes**
```bash
git clone https://github.com/tridge/MAVProxy
git clone https://github.com/tridge/mavlink
```
ejecuta el comando de configuración en ambos directorios
```
sudo python setup.py build install
```

---
Obten la rama de APM que compila en Mac OS ([este commit](https://github.com/erlerobot/ardupilot/commit/337bd7bf1f6d285934e887ddb06563960d0aa157) es importante):
```bash
git clone https://github.com/erlerobot/ardupilot
cd ardupilot
git checkout macos
cd ArduCopter
make configure
make sitl
```

Fuente: [drones-discuss](https://groups.google.com/forum/#!searchin/drones-discuss/SITL$20mac$20os/drones-discuss/kLx9kJAT9As/5UnGEn-mSQsJ)
