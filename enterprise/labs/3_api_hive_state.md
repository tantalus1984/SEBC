### Stop
```curl -u tantalus1984:cloudera -X POST 'http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v2/cluster/tantalus1984/services/hive/commands/stop'```
```{
  "id" : 618,
  "name" : "Stop",
  "startTime" : "2017-03-08T10:18:41.630Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}```

### Start
```curl -u tantalus1984:cloudera -X POST 'http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v2/clusters/tantalus1984/services/hive/commands/start'```
```{
  "id" : 622,
  "name" : "Start",
  "startTime" : "2017-03-08T10:20:55.461Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}```

### Check
```curl -u tantalus1984:cloudera 'http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v2/clusters/tantalus1984/services/hive'```
```{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "https://ip-172-31-26-85.eu-central-1.compute.internal:7183/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}``` 
