# nagios-check_handlersocket_latency


This is a Nagios plugin for HandlerSocket. This plugin checks read latency. 

# Usage 

```
% check_handlersocket_latency -w [waring seconds] -c [critical seconds] -host [hostname]
% check_handlersocket_latency -w 0.70 -c 1.00 -host localhost
```

This plugin checks database "mysql", column of "Host" and value of "localhost" from user table.
You can cahnge default value by command option.
Default value is here.

```
host: localhost
port: 9998
database: mysql
table: user
index: PRIMARY
columns: Host
value: localhost
```

# Link


https://github.com/DeNA/HandlerSocket-Plugin-for-MySQL
