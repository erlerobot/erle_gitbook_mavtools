# SITL

The SITL (Software In The Loop) simulator allows you to run APM  without any hardware. It is a build of the autopilot code using an ordinary C++ compiler and giving you a native executable that allows you to test the behaviour of the code without hardware.

![](http://dev.ardupilot.com/wp-content/uploads/sites/6/2013/04/SITL_Linux.png)

### Installation Ubuntu
Refer to the [APM wiki](http://dev.ardupilot.com/wiki/setting-up-sitl-on-linux/) for installation instructions.

#### Launch the simulator
```bash
sim_vehicle.sh -w
```

### Instalation Mac OS
Install just the command line tools for OSX including GCC then get modules installed to Python:
```bash
sudo easy_install pip
sudo pip install pexpect
sudo pip install pyserial
```
Install MAVLink and MAVProxy:
```bash
sudo pip install pymavlink MAVProxy
```

---

**(or) install MAVLink and MAVProxy from source**
```bash
git clone https://github.com/tridge/MAVProxy
git clone https://github.com/tridge/mavlink
```
run this setup command in both directories
```
sudo python setup.py build install
```

---

Get the APM branch that compiles in Mac OS ([this commit](https://github.com/erlerobot/ardupilot/commit/337bd7bf1f6d285934e887ddb06563960d0aa157) is relevant):
```bash
git clone https://github.com/erlerobot/ardupilot
cd ardupilot
git checkout macos
cd ArduCopter
make configure
make sitl
```

Source: [drones-discuss](https://groups.google.com/forum/#!searchin/drones-discuss/SITL$20mac$20os/drones-discuss/kLx9kJAT9As/5UnGEn-mSQsJ)
