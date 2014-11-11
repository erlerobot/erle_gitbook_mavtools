# Performance

The performance of the APM instance running in the Linux machine can be monitored using the `SCHED_DEBUG` APM parameter.

According to the [wiki](http://copter.ardupilot.com/wiki/arducopter-parameters/#Scheduler_debug_level_SCHED_DEBUG):

```
Set to non-zero to enable scheduler debug messages. When set to show “Slips” the scheduler will display a message whenever a scheduled task is delayed due to too much CPU load. When set to ShowOverruns the scheduled will display a message whenever a task takes longer than the limit promised in the task table.
```

|VALUE	| MEANING |
|-----|-----|
|0	|Disabled|
|2	|ShowSlips|
|3	|ShowOverruns|

Setting up option 3 using `param set SCHED_DEBUG 3` outputs something like:
```bash
Scheduler overrun task[15] (34/20)
Scheduler overrun task[16] (26/20)
PERF: 4/1000 21647
PERF: 3/1000 23464
Flight battery warning
PERF: 5/1000 21938
Scheduler overrun task[5] (15/10)
PERF: 4/1000 23464
PERF: 4/1000 21506
Scheduler overrun task[15] (24/20)
PERF: 5/1000 22517
PERF: 3/1000 23606
Scheduler overrun task[5] (14/10)
Scheduler overrun task[16] (23/20)
PERF: 4/1000 21146
Flight battery warning
```

## Understanding the output

### PERF

```
PERF: 4/1000 23464
```
should be understood as:
>4 out of 1000 tasks took longer than expected (20000 us since we are running at 50 Hz)

### Overrun task

```
Scheduler overrun task[16] (23/20)
```
> task 16 was overrun by 23  versus the 20 that was expected to take.

Refer to http://dev.ardupilot.com/wiki/code-overview-scheduling-your-new-code-to-run-intermittently/ for understanding more about tasks.
