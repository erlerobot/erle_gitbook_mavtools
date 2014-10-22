#mavlogdump

Esta herramienta permite convertir un archivo de log binario en un fichero capaz de ser leido. La salida del programa se mostrará por la salida estandar. Esta herramienta puede usarse como:

Uso:
```bash
mavlogdump.py [options] <LOGFILE>
```

Opciones:
```bash
  -h, --help            show this help message and exit
  --no-timestamps       Log doesn't have timestamps
  --planner             use planner file format
  --robust              Enable robust parsing (skip over bad data)
  -f, --follow          keep waiting for more data at end of file
  --condition=CONDITION
                        select packets by condition
  -q, --quiet           don't display packets
  -o OUTPUT, --output=OUTPUT
                        output matching packets to give file
  -p, --parms           preserve parameters in output with -o
  --format=FORMAT       Change the output format between 'standard', 'json',
                        and 'csv'. For the CSV output, you must supply types
                        that you want.
  --csv_sep=CSV_SEP     Select the delimiter between columns for the output
                        CSV file. Use 'tab' to specify tabs. Only applies when
                        --format=csv
  --types=TYPES         types of messages (comma separated)
  --dialect=DIALECT     MAVLink dialect
  --zero-time-base      use Z time base for DF logs
```

Dado un vuelo con el nombre `1.BIN` y que deseamos ver su contenido, el procedimiento es el siguiente:


Ahora podemos ser capaces de ver el contenido del log tan solo leyendo el fichero:

```bash
mavlogdump.py 1.BIN > 1.BIN.txt
```

Ahora puedes revisar el contenido de 1.BIN.txt:
```bash
cat 1.BIN.txt
```