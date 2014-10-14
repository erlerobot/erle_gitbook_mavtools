# Where I can find a log file?

The fligth logs are stored at `rootfs`. A new log file is generated when the autopilot is started and the system is armed.

##SDCARD
If we connect the SDcard to our PC and we introduce the command `mount` we can see where has it been mounted. For example at `/media/rootfs`.
Doing :
```
cd /media/rootfs
```
We get located at the `rootfs` partition. The logs get tored at `/var`. Now we want to recover the last log from, for example, `ArduRover`:

```
cd /var/APM/logs
```
Here we find all the `APMrover2`, `ArduCopter` or `ArduPlane` logs and a file called `lastlog.txt`.
```
less lastlog.txt
```
shows us the name of the last log, let's suppose `5.BIN`.
Now we can copy it to the `Logs` folder at our home, by doing:
```
cp 5.BIN ~/Logs
```

##SSH

We can connect with the board through the USB or WIFI and navigate into the filesystem to find an interesting log.

If we want to connect with the board via USB. First at all, it's necessary to check the IP because the DHCP server sometimes fails. When you connect the board a new interface is created. It's possible to check the interface with the command `ifconfig`. If you need to force the IP you need to type in the shell (in this case `eth2` is the network interfaces that creates the BeagleBone):

```
sudo ifconfig eth2 192.168.7.2
```

Now, you can connect with the board via USB:

```
ssh root@192.168.7.2
```

or via Wifi:

```
ssh root@111.0.0.1
```

It's possible to copy a file using `scp` in your computer:

```
scp root@192.168.7.2:/var/APM/logs/1.BIN ~/LOGS
```

#Upload your log

The logs generally are added to [https://github.com/erlerobot/drones_logs](https://github.com/erlerobot/drones_logs)
