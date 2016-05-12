# nagios-check_handlersocket_latency


This is a Nagios plugin for HandlerSocket(https://github.com/DeNA/HandlerSocket-Plugin-for-MySQL).   
This plugin checks read latency. 

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


For exsample, if you have a table like this.

```
mysql> use sampledb;
mysql> create table personal(id int PRIMARY KEY, name varchar(20));
mysql> INSERT INTO personal (id,name) VALUES (100, "test");
```

You can check your table by this option.

```
$ ./check_handlersocket_latency -w 0.005 -c 0.020 -host localhost -database sampledb -table personal -columns id -value 100
OK: HandlerSocket read response in 0.001996 s|latency_seconds=0.001996
```


