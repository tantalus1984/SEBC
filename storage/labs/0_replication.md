### Trying to distcp with horizonnet's cluster. 
* distcp throws error that it cannot replicate blocks. 
* Assuming that DataNode's internal DNS is not known by horizonnet's cluster. 
* Switching HDFS DataNodes to use Hostnames instead of IPs to relay DNS resolution to horizonnet's distcp. 
* Also binding NameNode and DataNode to wildcard interface (multihoming). 
* Datanodes use internal DNS names that differ from EC2 external DNS names. 
* Would need to override Datanode's DNS throug maintaing /etc/hosts for every node. Not doing this, because now we are really getting towards hacking the solution together. It is also to be expected that Host Inspector would fail afterwards, since canoncial hostname differs from DNS. Changing hostnames in Cloudera can be done, but is something Cloudera does not recommend. It involves changing db.properties of scm-server, changing database names for CDH roles, such as Oozie, Sentry, Hive, Hue, etc., changing certificates... 
* The correct way of doing this would be to place both clusters into the same subnet or create a route between the subnets of both clusters.

### distcp'ing to own cluster instead
* teragen 500MB
``` hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen 5000000 /user/tantalus1984/teragen```
* checking generated blocks and files
``` hdfs fsck /user/tantalus1984/teragen -files -blocks```

* distcp'ing
``` hadoop distcp hdfs://nameservice1/user/tantalus1984/teragen hdfs://nameservice1/user/tantalus1984/teragen.copy ```
* comparing copied blocks and files with original
``` hdfs fsck /user/tantalus1984/teragen.copy -files -blocks ```

### distcp'ing with Cloudera BDR
* create a new peer (in this case the own cluster)
* create a new replication schedule for "HDFS replication"
* specify source and destinatio
* set schedule to immediate
* do a "Dry Run"
* click "Run Now"
