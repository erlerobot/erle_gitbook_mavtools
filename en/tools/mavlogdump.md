# mavlogdump

This tool allows to convert a binary log into a readable file. When no output is provided it dumps the content in the standart output. The tool can be used as:

```bash
avtools$ mavlogdump.py -h
Usage: mavlogdump.py [options] <LOGFILE>

Options:
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

Given that we have a flight log called `1.BIN` and we wish to see its content, the procedure will be:
```bash
mavlogdump.py 1.BIN > 1.BIN.txt
```
Now you can see the content of `1.BIN.txt`:
```bash
cat 1.BIN.txt
```
