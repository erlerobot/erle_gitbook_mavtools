# Modules

MAVProxy se puede extender con modulos. Estos se ejecutan en hilos paralelos al programa principal con el fin de mantener la estabilidad.

Los módulos pueden incluir osas como interfaces de usuario, diagnóstico y monitorización.

#### Gestión de los módulos
Los módulos pueden necesitar ser cargados antes de ser usados. Utilizando los siguiente comandos:

```
module load <modulename>
```

Otros comandos para la gestión de módulos: desactivar, recargar o mostrar la lista de los módulos actualmente cargados:

```
module unload modulename
module reload modulename
module list
```