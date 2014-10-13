# Conection

MAVProxy only needs to address of the USB port or network address to connect to.

####--master
Specifies which port (serial, USB or network address/port) the UAV is communicating on.

####Over USB

If there is only 1 APM connected, the `--master` is not required. MAVProxy will autodetect correct port.
```
mavproxy.py --master=/dev/ttyUSB0
```
The baud rate will need to match the serial link being used. It is usually 57600 baud.

```
mavproxy.py --master=/dev/ttyUSB0 --baudrate=57600
```


####Over Network
The address to connect to must be your own IP address.

```
mavproxy.py --master=192.168.1.1:14550
```
