# Modules

MAVProxy can be extended with modules. These run in parallel threads to the main MAVProxy program in order to maintain overall stability.

Modules can include such things a GUI elements and diagnostic and monitoring applications.

####Module Management
Modules need to be loaded before they can be used. The following command can be used:

```
module load modulename
```

Other management commands for unloading, reloading and listing currently loaded modules include:

```
module unload modulename
module reload modulename
module list
```