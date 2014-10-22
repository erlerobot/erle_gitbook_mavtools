# Parameters

Parameters refer to the settings and configuration of the APM. The following commands can be used to view and change the parameters:

#### param show
View all current parameters on the APM.

```bash
param show
```

####param set
Change a specified parameter to a particular value.

```bash
param set FLTMODE1 9
```

####param save
Save all current parameters on the APM to file.

```bash
param save filename.parm
```

####param load
Load parameters from file to APM. Only the parameters in the file will be overwritten.

```bash
param load filename.parm
```

####param diff
View the differences between the parameters in a file and what is currently on the APM.

```bash
param diff filename.parm
```

####Wildcards
Any of the above commands can be filtered by using wildcards, if only a particular subset of parameters needs to be manipulated.

```bash
param show FLTMODE*
param load RC1*
```

####param download
Downloads the parameter definitions from the Internet and cache.

```bash
param download
```
####param help
Shows further information (usage, notes) of the specified parameter.
```bash
param help FLTMODE1
```
