### list user home dirs in HDFS
```
[root@ip-172-31-20-21 ~]# hdfs dfs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop           0 2017-03-10 04:24 /user/history
drwxrwxr-t   - hive    hive             0 2017-03-10 04:25 /user/hive
drwxrwxr-x   - hue     hue              0 2017-03-10 04:25 /user/hue
drwx------   - neymar  neymar           0 2017-03-10 04:31 /user/neymar
drwxrwxr-x   - oozie   oozie            0 2017-03-10 04:26 /user/oozie
drwx------   - ronaldo ronaldo          0 2017-03-10 04:31 /user/ronaldo
```

### hosts via API v14
```
{
  "items" : [ {
    "hostId" : "f82b7ec3-704a-4024-8c71-311a61185f6b",
    "ipAddress" : "172.31.17.194",
    "hostname" : "ip-172-31-17-194.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-106.eu-central-1.compute.internal:7180/cmf/hostRedirect/f82b7ec3-704a-4024-8c71-311a61185f6b",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "a84ad59f-636e-4a85-a82f-95bda8abbe98",
    "ipAddress" : "172.31.19.63",
    "hostname" : "ip-172-31-19-63.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-106.eu-central-1.compute.internal:7180/cmf/hostRedirect/a84ad59f-636e-4a85-a82f-95bda8abbe98",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "a5eb0e0c-f4a2-437d-a1e5-f62e01a5c600",
    "ipAddress" : "172.31.20.100",
    "hostname" : "ip-172-31-20-100.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-106.eu-central-1.compute.internal:7180/cmf/hostRedirect/a5eb0e0c-f4a2-437d-a1e5-f62e01a5c600",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "7f9c732b-c972-46f1-9dd8-f0262565a209",
    "ipAddress" : "172.31.20.21",
    "hostname" : "ip-172-31-20-21.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-106.eu-central-1.compute.internal:7180/cmf/hostRedirect/7f9c732b-c972-46f1-9dd8-f0262565a209",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "d1a8d222-2cc4-440e-9127-aa5ca3226226",
    "ipAddress" : "172.31.23.106",
    "hostname" : "ip-172-31-23-106.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-106.eu-central-1.compute.internal:7180/cmf/hostRedirect/d1a8d222-2cc4-440e-9127-aa5ca3226226",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  } ]
}
```
