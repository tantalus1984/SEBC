### hostname of the mysql server
ip-172-31-20-21.eu-central-1.compute.internal

### mysql version
```
mysql> select @@version;
+-----------+
| @@version |
+-----------+
| 5.6.35    |
+-----------+
1 row in set (0.00 sec)
```

### list databases
```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
```

