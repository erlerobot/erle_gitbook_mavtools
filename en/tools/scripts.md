# Scripts

MAVProxy is capable of executing a script (of MAVProxy commands) on startup. This can save the effort of (re)setting up the MAVProxy environment for each flight.

A script (mavinit.scr) should be placed in an aircraft directory (ie. MAVProxy/Aircraftname/mavinit.scr) containing the commands. Any normal MAVProxy commands can be placed in here. Note that the --aircraft option must be used, in order for MAVProxy to find the script in the appropriate aircraft directory.

Alternatively, a .mavinit.scr can be placed in the user's home directory (ie. /home/username in Linux or /Users/username in MACOS) and will be loaded with MAVProxy regardless of the --aircraft option.

Also you can load the script by typing:

```
script mavinit.scr
```

In this particular script, aliases are used as shortcuts to common commands.

For example:
```
@alias add grp g degrees(ATTITUDE.roll) degrees(ATTITUDE.pitch)
```
in the mavinit.scr will allow the user to graph the current pitch and roll in degrees by typing

````
grp
```

instead of

```
graph degrees(ATTITUDE.roll) degrees(ATTITUDE.pitch)
```
