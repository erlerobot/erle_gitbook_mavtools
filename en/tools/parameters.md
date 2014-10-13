# Parameters

Parameters refer to the settings and configuration of the APM. The following commands can be used to view and change the parameters:

#### param show
View all current parameters on the APM.

```
param show
```

####param set
Change a specified parameter to a particular value.

```
param set FLTMODE1 9
```

####param save
Save all current parameters on the APM to file.

```
param save filename.parm
```

####param load
Load parameters from file to to APM. Only the parameters in the file will be overwritten.

```
param load filename.parm
```

####param diff
View the differences between the parameters in a file and what is currently on the APM.

```
param diff filename.parm
```

####Wildcards
Any of the above commands can be filtered by using wildcards, if only a particular subset of parameters needs to be manipulated.

```
param show FLTMODE*
param load RC1*
```

####param download
Downloads the parameter definitions from the Internet and cache.

```
param download
```
####param help
Shows further information (usage, notes) of the specified parameter.
```
param help FLTMODE1
```
