# Parameters
Parámetros se refieren a los valores y la configuración de la APM. Los siguientes comandos se pueden utilizar para ver y cambiar los parámetros:

#### param show
Ver todos lo parámetros actuales en APM.

```
param show
```

####param set
Cambia un valor específico con un valor en particular.

```
param set FLTMODE1 9
```

####param save
Guarda todos los parámetros de APM en un fichero.

```
param save filename.parm
```

####param load
Carga los parámetros desde un fichero a APM
Load parameters from file to  APM. Only the parameters in the file will be overwritten.

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
