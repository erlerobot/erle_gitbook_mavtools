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
Carga los parámetros desde un fichero a APM. Solo los parámetros que pueden ser sobreescritos.

```
param load filename.parm
```

####param diff
Ver las diferencias entre los parámetros en un archivo y lo que hay actualmente en APM.

```
param diff filename.parm
```

####Wildcards
Cualquiera de los comandos anteriores se pueden filtrar mediante el uso de *Wildcards* (comodines), si sólo un subconjunto particular de parámetros tiene que ser manipulado.

```
param show FLTMODE*
param load RC1*
```

####param download
Descarga los parámetros de Internet

```
param download
```
####param help

Muestra más información (de uso, notas) del parámetro especificado.
```
param help FLTMODE1
```
