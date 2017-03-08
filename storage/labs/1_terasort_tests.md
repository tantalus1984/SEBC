### Generating 1GB (my cluster is fairly small) of teragen data with 4 mappers and block size = 32 MB (1024x1024x32)
* ```time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen -Ddfs.block.size=33554432 -Dmapreduce.job.maps=4 10000000 /user/tantalus1984/teragen1g```

### Generation took 22 seconds
* real	0m22.066s
* user	0m5.435s
* sys	0m0.286s


### Sorting 1GB of teragen data.
* ```time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar terasort /user/tantalus1984/teragen1g /user/tantalus1984/teragen1g.sorted```

### Sorting took 59 seconds

* real	0m58.991s
* user	0m7.726s
* sys	0m0.323s
