### teragen command and output
```
[neymar@ip-172-31-20-21 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Ddfs.block.size=16777216 65536000 /user/neymar/tgen640
17/03/10 04:44:06 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-17-194.eu-central-1.compute.internal/172.31.17.194:8032
17/03/10 04:44:07 INFO terasort.TeraSort: Generating 65536000 using 8
17/03/10 04:44:07 INFO mapreduce.JobSubmitter: number of splits:8
17/03/10 04:44:07 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/03/10 04:44:07 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489137862937_0001
17/03/10 04:44:08 INFO impl.YarnClientImpl: Submitted application application_1489137862937_0001
17/03/10 04:44:08 INFO mapreduce.Job: The url to track the job: http://ip-172-31-17-194.eu-central-1.compute.internal:8088/proxy/application_1489137862937_0001/
17/03/10 04:44:08 INFO mapreduce.Job: Running job: job_1489137862937_0001
17/03/10 04:44:15 INFO mapreduce.Job: Job job_1489137862937_0001 running in uber mode : false
17/03/10 04:44:15 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 04:44:28 INFO mapreduce.Job:  map 7% reduce 0%
17/03/10 04:44:29 INFO mapreduce.Job:  map 10% reduce 0%
17/03/10 04:44:30 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 04:44:31 INFO mapreduce.Job:  map 16% reduce 0%
17/03/10 04:44:32 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 04:44:33 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 04:44:35 INFO mapreduce.Job:  map 26% reduce 0%
17/03/10 04:44:36 INFO mapreduce.Job:  map 27% reduce 0%
17/03/10 04:44:39 INFO mapreduce.Job:  map 28% reduce 0%
17/03/10 04:44:43 INFO mapreduce.Job:  map 29% reduce 0%
17/03/10 04:44:46 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 04:44:52 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 04:44:55 INFO mapreduce.Job:  map 33% reduce 0%
17/03/10 04:44:58 INFO mapreduce.Job:  map 36% reduce 0%
17/03/10 04:45:01 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 04:45:05 INFO mapreduce.Job:  map 38% reduce 0%
17/03/10 04:45:14 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 04:45:15 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 04:45:17 INFO mapreduce.Job:  map 41% reduce 0%
17/03/10 04:45:22 INFO mapreduce.Job:  map 43% reduce 0%
17/03/10 04:45:25 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 04:45:28 INFO mapreduce.Job:  map 45% reduce 0%
17/03/10 04:45:32 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 04:45:35 INFO mapreduce.Job:  map 47% reduce 0%
17/03/10 04:45:39 INFO mapreduce.Job:  map 48% reduce 0%
17/03/10 04:45:43 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 04:45:46 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 04:45:50 INFO mapreduce.Job:  map 52% reduce 0%
17/03/10 04:45:56 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 04:45:59 INFO mapreduce.Job:  map 54% reduce 0%
17/03/10 04:46:02 INFO mapreduce.Job:  map 55% reduce 0%
17/03/10 04:46:04 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 04:46:05 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 04:46:07 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 04:46:08 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 04:46:10 INFO mapreduce.Job:  map 65% reduce 0%
17/03/10 04:46:11 INFO mapreduce.Job:  map 66% reduce 0%
17/03/10 04:46:12 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 04:46:13 INFO mapreduce.Job:  map 68% reduce 0%
17/03/10 04:46:14 INFO mapreduce.Job:  map 69% reduce 0%
17/03/10 04:46:15 INFO mapreduce.Job:  map 71% reduce 0%
17/03/10 04:46:16 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 04:46:18 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 04:46:19 INFO mapreduce.Job:  map 75% reduce 0%
17/03/10 04:46:21 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 04:46:23 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 04:46:24 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 04:46:25 INFO mapreduce.Job:  map 81% reduce 0%
17/03/10 04:46:26 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 04:46:27 INFO mapreduce.Job:  map 84% reduce 0%
17/03/10 04:46:29 INFO mapreduce.Job:  map 85% reduce 0%
17/03/10 04:46:30 INFO mapreduce.Job:  map 87% reduce 0%
17/03/10 04:46:32 INFO mapreduce.Job:  map 89% reduce 0%
17/03/10 04:46:33 INFO mapreduce.Job:  map 90% reduce 0%
17/03/10 04:46:34 INFO mapreduce.Job:  map 91% reduce 0%
17/03/10 04:46:35 INFO mapreduce.Job:  map 92% reduce 0%
17/03/10 04:46:36 INFO mapreduce.Job:  map 93% reduce 0%
17/03/10 04:46:38 INFO mapreduce.Job:  map 95% reduce 0%
17/03/10 04:46:39 INFO mapreduce.Job:  map 97% reduce 0%
17/03/10 04:46:41 INFO mapreduce.Job:  map 98% reduce 0%
17/03/10 04:46:42 INFO mapreduce.Job:  map 100% reduce 0%
17/03/10 04:46:42 INFO mapreduce.Job: Job job_1489137862937_0001 completed successfully
17/03/10 04:46:42 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=983800
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=682
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=32
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters 
		Launched map tasks=8
		Other local map tasks=8
		Total time spent by all maps in occupied slots (ms)=1122389
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=1122389
		Total vcore-seconds taken by all map tasks=1122389
		Total megabyte-seconds taken by all map tasks=1149326336
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=682
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1750
		CPU time spent (ms)=140130
		Physical memory (bytes) snapshot=2691059712
		Virtual memory (bytes) snapshot=12521238528
		Total committed heap usage (bytes)=2772434944
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
```


### time
```
real	2m38.586s
user	0m6.248s
sys	0m0.325s
```

### listing /user/neymar/tgen640
```
[neymar@ip-172-31-20-21 ec2-user]$ hdfs dfs -ls /user/neymar/tgen640
Found 9 items
-rw-r--r--   3 neymar neymar          0 2017-03-10 04:46 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 04:46 /user/neymar/tgen640/part-m-00007
```

### block report
```
[neymar@ip-172-31-20-21 ec2-user]$ hdfs fsck /user/neymar/tgen640 -blocks
Connecting to namenode via http://ip-172-31-17-194.eu-central-1.compute.internal:50070
FSCK started by neymar (auth:SIMPLE) from /172.31.20.21 for path /user/neymar/tgen640 at Fri Mar 10 04:48:14 EST 2017
.........Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	1
 Total files:	9
 Total symlinks:		0
 Total blocks (validated):	392 (avg. block size 16718367 B)
 Minimally replicated blocks:	392 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Mar 10 04:48:14 EST 2017 in 17 milliseconds


The filesystem under path '/user/neymar/tgen640' is HEALTHY
```
