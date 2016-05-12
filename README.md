# nagios-check_handlersocket_latency


This is a Nagios plugin for HandlerSocket. This plugin checks read latency. 

# Usage 

```
% check_handlersocket_latency -w [waring seconds] -c [critical seconds] -host [hostname]
% check_handlersocket_latency -w 0.70 -c 1.00 -host localhost
```

This plugin checks value of "localhost" and column of "Host" from user table.


# Link


https://github.com/DeNA/HandlerSocket-Plugin-for-MySQL
