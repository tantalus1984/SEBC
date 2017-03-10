### running terasort with neymar
```
[neymar@ip-172-31-20-21 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.reduces=2  /user/neymar/tgen640 /user/neymar/tsort640
17/03/10 05:27:39 INFO terasort.TeraSort: starting
17/03/10 05:27:41 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@TANTALUS.ES, renewer=yarn, realUser=, issueDate=1489141661386, maxDate=1489746461386, sequenceNumber=1, masterKeyId=4 on 172.31.17.194:8020
17/03/10 05:27:41 INFO security.TokenCache: Got dt for hdfs://ip-172-31-17-194.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.17.194:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@TANTALUS.ES, renewer=yarn, realUser=, issueDate=1489141661386, maxDate=1489746461386, sequenceNumber=1, masterKeyId=4)
17/03/10 05:27:41 INFO input.FileInputFormat: Total input paths to process : 8
Spent 587ms computing base-splits.
Spent 8ms computing TeraScheduler splits.
Computing input splits took 596ms
Sampling 10 splits of 392
Making 2 from 100000 sampled records
Computing parititions took 830ms
Spent 1429ms computing partitions.
17/03/10 05:27:42 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-17-194.eu-central-1.compute.internal/172.31.17.194:8032
17/03/10 05:27:43 INFO mapreduce.JobSubmitter: number of splits:392
17/03/10 05:27:43 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489141569701_0001
17/03/10 05:27:43 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.17.194:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@TANTALUS.ES, renewer=yarn, realUser=, issueDate=1489141661386, maxDate=1489746461386, sequenceNumber=1, masterKeyId=4)
17/03/10 05:27:44 INFO impl.YarnClientImpl: Submitted application application_1489141569701_0001
17/03/10 05:27:44 INFO mapreduce.Job: The url to track the job: http://ip-172-31-17-194.eu-central-1.compute.internal:8088/proxy/application_1489141569701_0001/
17/03/10 05:27:44 INFO mapreduce.Job: Running job: job_1489141569701_0001
17/03/10 05:27:53 INFO mapreduce.Job: Job job_1489141569701_0001 running in uber mode : false
17/03/10 05:27:53 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 05:28:04 INFO mapreduce.Job:  map 1% reduce 0%
17/03/10 05:28:10 INFO mapreduce.Job:  map 2% reduce 0%
17/03/10 05:28:14 INFO mapreduce.Job:  map 3% reduce 0%
17/03/10 05:28:19 INFO mapreduce.Job:  map 4% reduce 0%
17/03/10 05:28:23 INFO mapreduce.Job:  map 5% reduce 0%
17/03/10 05:28:26 INFO mapreduce.Job:  map 6% reduce 0%
17/03/10 05:28:29 INFO mapreduce.Job:  map 7% reduce 0%
17/03/10 05:28:37 INFO mapreduce.Job:  map 8% reduce 0%
17/03/10 05:28:38 INFO mapreduce.Job:  map 9% reduce 0%
17/03/10 05:28:41 INFO mapreduce.Job:  map 10% reduce 0%
17/03/10 05:28:48 INFO mapreduce.Job:  map 11% reduce 0%
17/03/10 05:28:51 INFO mapreduce.Job:  map 12% reduce 0%
17/03/10 05:28:53 INFO mapreduce.Job:  map 13% reduce 0%
17/03/10 05:28:58 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 05:29:02 INFO mapreduce.Job:  map 15% reduce 0%
17/03/10 05:29:06 INFO mapreduce.Job:  map 16% reduce 0%
17/03/10 05:29:11 INFO mapreduce.Job:  map 17% reduce 0%
17/03/10 05:29:15 INFO mapreduce.Job:  map 18% reduce 0%
17/03/10 05:29:19 INFO mapreduce.Job:  map 19% reduce 0%
17/03/10 05:29:24 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 05:29:26 INFO mapreduce.Job:  map 21% reduce 0%
17/03/10 05:29:29 INFO mapreduce.Job:  map 22% reduce 0%
17/03/10 05:29:34 INFO mapreduce.Job:  map 23% reduce 0%
17/03/10 05:29:38 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 05:29:41 INFO mapreduce.Job:  map 25% reduce 0%
17/03/10 05:29:46 INFO mapreduce.Job:  map 26% reduce 0%
17/03/10 05:29:49 INFO mapreduce.Job:  map 27% reduce 0%
17/03/10 05:29:51 INFO mapreduce.Job:  map 28% reduce 0%
17/03/10 05:29:57 INFO mapreduce.Job:  map 29% reduce 0%
17/03/10 05:30:01 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 05:30:05 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 05:30:08 INFO mapreduce.Job:  map 32% reduce 0%
17/03/10 05:30:13 INFO mapreduce.Job:  map 33% reduce 0%
17/03/10 05:30:16 INFO mapreduce.Job:  map 34% reduce 0%
17/03/10 05:30:21 INFO mapreduce.Job:  map 35% reduce 0%
17/03/10 05:30:24 INFO mapreduce.Job:  map 36% reduce 0%
17/03/10 05:30:26 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 05:30:31 INFO mapreduce.Job:  map 38% reduce 0%
17/03/10 05:30:34 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 05:30:39 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 05:30:41 INFO mapreduce.Job:  map 41% reduce 0%
17/03/10 05:30:47 INFO mapreduce.Job:  map 42% reduce 0%
17/03/10 05:30:49 INFO mapreduce.Job:  map 43% reduce 0%
17/03/10 05:30:53 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 05:30:57 INFO mapreduce.Job:  map 45% reduce 0%
17/03/10 05:31:00 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 05:31:06 INFO mapreduce.Job:  map 47% reduce 0%
17/03/10 05:31:09 INFO mapreduce.Job:  map 48% reduce 0%
17/03/10 05:31:15 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 05:31:16 INFO mapreduce.Job:  map 50% reduce 0%
17/03/10 05:31:20 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 05:31:24 INFO mapreduce.Job:  map 52% reduce 0%
17/03/10 05:31:28 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 05:31:35 INFO mapreduce.Job:  map 54% reduce 0%
17/03/10 05:31:36 INFO mapreduce.Job:  map 55% reduce 0%
17/03/10 05:31:42 INFO mapreduce.Job:  map 56% reduce 0%
17/03/10 05:31:44 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 05:31:47 INFO mapreduce.Job:  map 58% reduce 0%
17/03/10 05:31:53 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 05:31:56 INFO mapreduce.Job:  map 60% reduce 0%
17/03/10 05:32:01 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 05:32:03 INFO mapreduce.Job:  map 62% reduce 0%
17/03/10 05:32:09 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 05:32:10 INFO mapreduce.Job:  map 64% reduce 0%
17/03/10 05:32:16 INFO mapreduce.Job:  map 65% reduce 0%
17/03/10 05:32:19 INFO mapreduce.Job:  map 66% reduce 0%
17/03/10 05:32:21 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 05:32:28 INFO mapreduce.Job:  map 68% reduce 0%
17/03/10 05:32:30 INFO mapreduce.Job:  map 69% reduce 0%
17/03/10 05:32:35 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 05:32:38 INFO mapreduce.Job:  map 71% reduce 0%
17/03/10 05:32:42 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 05:32:47 INFO mapreduce.Job:  map 73% reduce 0%
17/03/10 05:32:50 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 05:32:53 INFO mapreduce.Job:  map 75% reduce 0%
17/03/10 05:32:56 INFO mapreduce.Job:  map 76% reduce 0%
17/03/10 05:33:02 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 05:33:05 INFO mapreduce.Job:  map 78% reduce 0%
17/03/10 05:33:08 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 05:33:15 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 05:33:16 INFO mapreduce.Job:  map 81% reduce 0%
17/03/10 05:33:21 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 05:33:26 INFO mapreduce.Job:  map 83% reduce 0%
17/03/10 05:33:29 INFO mapreduce.Job:  map 83% reduce 3%
17/03/10 05:33:30 INFO mapreduce.Job:  map 84% reduce 3%
17/03/10 05:33:32 INFO mapreduce.Job:  map 84% reduce 4%
17/03/10 05:33:34 INFO mapreduce.Job:  map 84% reduce 7%
17/03/10 05:33:35 INFO mapreduce.Job:  map 85% reduce 9%
17/03/10 05:33:37 INFO mapreduce.Job:  map 85% reduce 10%
17/03/10 05:33:40 INFO mapreduce.Job:  map 86% reduce 11%
17/03/10 05:33:42 INFO mapreduce.Job:  map 86% reduce 12%
17/03/10 05:33:43 INFO mapreduce.Job:  map 86% reduce 14%
17/03/10 05:33:45 INFO mapreduce.Job:  map 87% reduce 15%
17/03/10 05:33:48 INFO mapreduce.Job:  map 87% reduce 16%
17/03/10 05:33:50 INFO mapreduce.Job:  map 88% reduce 16%
17/03/10 05:33:51 INFO mapreduce.Job:  map 88% reduce 18%
17/03/10 05:33:52 INFO mapreduce.Job:  map 89% reduce 19%
17/03/10 05:33:54 INFO mapreduce.Job:  map 89% reduce 20%
17/03/10 05:33:57 INFO mapreduce.Job:  map 89% reduce 21%
17/03/10 05:33:58 INFO mapreduce.Job:  map 89% reduce 23%
17/03/10 05:33:59 INFO mapreduce.Job:  map 90% reduce 23%
17/03/10 05:34:00 INFO mapreduce.Job:  map 90% reduce 24%
17/03/10 05:34:03 INFO mapreduce.Job:  map 91% reduce 24%
17/03/10 05:34:04 INFO mapreduce.Job:  map 91% reduce 26%
17/03/10 05:34:07 INFO mapreduce.Job:  map 92% reduce 28%
17/03/10 05:34:14 INFO mapreduce.Job:  map 93% reduce 29%
17/03/10 05:34:16 INFO mapreduce.Job:  map 94% reduce 29%
17/03/10 05:34:17 INFO mapreduce.Job:  map 94% reduce 30%
17/03/10 05:34:18 INFO mapreduce.Job:  map 94% reduce 31%
17/03/10 05:34:22 INFO mapreduce.Job:  map 95% reduce 31%
17/03/10 05:34:24 INFO mapreduce.Job:  map 95% reduce 32%
17/03/10 05:34:27 INFO mapreduce.Job:  map 96% reduce 32%
17/03/10 05:34:31 INFO mapreduce.Job:  map 97% reduce 32%
17/03/10 05:34:35 INFO mapreduce.Job:  map 98% reduce 32%
17/03/10 05:34:36 INFO mapreduce.Job:  map 98% reduce 33%
17/03/10 05:34:39 INFO mapreduce.Job:  map 99% reduce 33%
17/03/10 05:34:42 INFO mapreduce.Job:  map 100% reduce 33%
17/03/10 05:34:43 INFO mapreduce.Job:  map 100% reduce 43%
17/03/10 05:34:45 INFO mapreduce.Job:  map 100% reduce 60%
17/03/10 05:34:46 INFO mapreduce.Job:  map 100% reduce 68%
17/03/10 05:34:48 INFO mapreduce.Job:  map 100% reduce 69%
17/03/10 05:34:49 INFO mapreduce.Job:  map 100% reduce 70%
17/03/10 05:34:51 INFO mapreduce.Job:  map 100% reduce 72%
17/03/10 05:34:52 INFO mapreduce.Job:  map 100% reduce 73%
17/03/10 05:34:54 INFO mapreduce.Job:  map 100% reduce 75%
17/03/10 05:34:55 INFO mapreduce.Job:  map 100% reduce 76%
17/03/10 05:34:57 INFO mapreduce.Job:  map 100% reduce 78%
17/03/10 05:34:58 INFO mapreduce.Job:  map 100% reduce 80%
17/03/10 05:35:00 INFO mapreduce.Job:  map 100% reduce 81%
17/03/10 05:35:01 INFO mapreduce.Job:  map 100% reduce 83%
17/03/10 05:35:03 INFO mapreduce.Job:  map 100% reduce 84%
17/03/10 05:35:04 INFO mapreduce.Job:  map 100% reduce 86%
17/03/10 05:35:06 INFO mapreduce.Job:  map 100% reduce 87%
17/03/10 05:35:07 INFO mapreduce.Job:  map 100% reduce 89%
17/03/10 05:35:09 INFO mapreduce.Job:  map 100% reduce 90%
17/03/10 05:35:10 INFO mapreduce.Job:  map 100% reduce 91%
17/03/10 05:35:12 INFO mapreduce.Job:  map 100% reduce 93%
17/03/10 05:35:13 INFO mapreduce.Job:  map 100% reduce 95%
17/03/10 05:35:15 INFO mapreduce.Job:  map 100% reduce 96%
17/03/10 05:35:17 INFO mapreduce.Job:  map 100% reduce 98%
17/03/10 05:35:18 INFO mapreduce.Job:  map 100% reduce 99%
17/03/10 05:35:19 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 05:35:19 INFO mapreduce.Job: Job job_1489141569701_0001 completed successfully
17/03/10 05:35:19 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=2944087347
		FILE: Number of bytes written=5857664395
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=6553661152
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=1182
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=392
		Launched reduce tasks=2
		Data-local map tasks=392
		Total time spent by all maps in occupied slots (ms)=3452277
		Total time spent by all reduces in occupied slots (ms)=238638
		Total time spent by all map tasks (ms)=3452277
		Total time spent by all reduce tasks (ms)=238638
		Total vcore-seconds taken by all map tasks=3452277
		Total vcore-seconds taken by all reduce tasks=238638
		Total megabyte-seconds taken by all map tasks=3535131648
		Total megabyte-seconds taken by all reduce tasks=244365312
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Map output bytes=6684672000
		Map output materialized bytes=2864261894
		Input split bytes=61152
		Combine input records=0
		Combine output records=0
		Reduce input groups=65536000
		Reduce shuffle bytes=2864261894
		Reduce input records=65536000
		Reduce output records=65536000
		Spilled Records=131072000
		Shuffled Maps =784
		Failed Shuffles=0
		Merged Map outputs=784
		GC time elapsed (ms)=35889
		CPU time spent (ms)=1381720
		Physical memory (bytes) snapshot=183218806784
		Virtual memory (bytes) snapshot=616341901312
		Total committed heap usage (bytes)=222970773504
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=6553600000
	File Output Format Counters 
		Bytes Written=6553600000
17/03/10 05:35:19 INFO terasort.TeraSort: done
```
