```bash
sudo su - nimbus
kinit nimbus
HDexample=/opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
time hadoop jar ${HDexample}/hadoop-mapreduce-examples.jar terasort \
      /user/nimbus/tgen /user/nimbus/tsort \
      -Dmapred.reduce.tasks=8000000
```

result
```
[nimbus@ip-172-31-23-52 ~]$ time hadoop jar ${HDexample}/hadoop-mapreduce-examples.jar terasort \
>       /user/nimbus/tgen /user/nimbus/tsort \
>       -Dmapred.reduce.tasks=8000000
17/08/11 06:25:08 INFO terasort.TeraSort: starting
17/08/11 06:25:10 INFO hdfs.DFSClient: Created token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447110023, maxDate=1503051910023, sequenceNumber=3, masterKeyId=2 on 172.31.21.175:8020
17/08/11 06:25:10 INFO security.TokenCache: Got dt for hdfs://ip-172-31-21-175.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447110023, maxDate=1503051910023, sequenceNumber=3, masterKeyId=2)
17/08/11 06:25:10 INFO input.FileInputFormat: Total input paths to process : 16
Spent 336ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 340ms
Sampling 10 splits of 112
Making 8 from 100000 sampled records
Computing parititions took 851ms
Spent 1194ms computing partitions.
17/08/11 06:25:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-175.eu-west-1.compute.internal/172.31.21.175:8032
17/08/11 06:25:11 INFO mapreduce.JobSubmitter: number of splits:112
17/08/11 06:25:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502446388515_0003
17/08/11 06:25:11 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447110023, maxDate=1503051910023, sequenceNumber=3, masterKeyId=2)
17/08/11 06:25:12 INFO impl.YarnClientImpl: Submitted application application_1502446388515_0003
17/08/11 06:25:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-175.eu-west-1.compute.internal:8088/proxy/application_1502446388515_0003/
17/08/11 06:25:12 INFO mapreduce.Job: Running job: job_1502446388515_0003
17/08/11 06:25:20 INFO mapreduce.Job: Job job_1502446388515_0003 running in uber mode : false
17/08/11 06:25:20 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 06:25:29 INFO mapreduce.Job:  map 2% reduce 0%
17/08/11 06:25:30 INFO mapreduce.Job:  map 4% reduce 0%
17/08/11 06:25:33 INFO mapreduce.Job:  map 5% reduce 0%
17/08/11 06:25:38 INFO mapreduce.Job:  map 7% reduce 0%
17/08/11 06:25:39 INFO mapreduce.Job:  map 9% reduce 0%
17/08/11 06:25:41 INFO mapreduce.Job:  map 11% reduce 0%
17/08/11 06:25:45 INFO mapreduce.Job:  map 13% reduce 0%
17/08/11 06:25:47 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 06:25:49 INFO mapreduce.Job:  map 15% reduce 0%
17/08/11 06:25:50 INFO mapreduce.Job:  map 16% reduce 0%
17/08/11 06:25:52 INFO mapreduce.Job:  map 18% reduce 0%
17/08/11 06:25:56 INFO mapreduce.Job:  map 20% reduce 0%
17/08/11 06:25:57 INFO mapreduce.Job:  map 21% reduce 0%
17/08/11 06:25:59 INFO mapreduce.Job:  map 23% reduce 0%
17/08/11 06:26:05 INFO mapreduce.Job:  map 26% reduce 0%
17/08/11 06:26:06 INFO mapreduce.Job:  map 29% reduce 0%
17/08/11 06:26:13 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 06:26:14 INFO mapreduce.Job:  map 34% reduce 0%
17/08/11 06:26:20 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 06:26:23 INFO mapreduce.Job:  map 39% reduce 0%
17/08/11 06:26:27 INFO mapreduce.Job:  map 41% reduce 0%
17/08/11 06:26:31 INFO mapreduce.Job:  map 42% reduce 0%
17/08/11 06:26:32 INFO mapreduce.Job:  map 45% reduce 0%
17/08/11 06:26:34 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 06:26:41 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 06:26:42 INFO mapreduce.Job:  map 52% reduce 0%
17/08/11 06:26:48 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 06:26:50 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 06:26:51 INFO mapreduce.Job:  map 57% reduce 0%
17/08/11 06:26:56 INFO mapreduce.Job:  map 59% reduce 0%
17/08/11 06:26:57 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 06:26:58 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 06:26:59 INFO mapreduce.Job:  map 63% reduce 0%
17/08/11 06:27:03 INFO mapreduce.Job:  map 64% reduce 0%
17/08/11 06:27:05 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 06:27:06 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 06:27:07 INFO mapreduce.Job:  map 68% reduce 0%
17/08/11 06:27:10 INFO mapreduce.Job:  map 70% reduce 0%
17/08/11 06:27:14 INFO mapreduce.Job:  map 71% reduce 0%
17/08/11 06:27:15 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 06:27:16 INFO mapreduce.Job:  map 73% reduce 0%
17/08/11 06:27:17 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 06:27:23 INFO mapreduce.Job:  map 77% reduce 0%
17/08/11 06:27:24 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 06:27:31 INFO mapreduce.Job:  map 84% reduce 0%
17/08/11 06:27:32 INFO mapreduce.Job:  map 85% reduce 0%
17/08/11 06:27:33 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 06:27:36 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 06:27:41 INFO mapreduce.Job:  map 90% reduce 0%
17/08/11 06:27:43 INFO mapreduce.Job:  map 90% reduce 7%
17/08/11 06:27:44 INFO mapreduce.Job:  map 91% reduce 11%
17/08/11 06:27:46 INFO mapreduce.Job:  map 93% reduce 11%
17/08/11 06:27:49 INFO mapreduce.Job:  map 93% reduce 12%
17/08/11 06:27:50 INFO mapreduce.Job:  map 94% reduce 12%
17/08/11 06:27:51 INFO mapreduce.Job:  map 95% reduce 12%
17/08/11 06:27:52 INFO mapreduce.Job:  map 96% reduce 12%
17/08/11 06:27:56 INFO mapreduce.Job:  map 97% reduce 12%
17/08/11 06:27:57 INFO mapreduce.Job:  map 98% reduce 12%
17/08/11 06:28:00 INFO mapreduce.Job:  map 99% reduce 12%
17/08/11 06:28:01 INFO mapreduce.Job:  map 100% reduce 12%
17/08/11 06:28:02 INFO mapreduce.Job:  map 100% reduce 16%
17/08/11 06:28:04 INFO mapreduce.Job:  map 100% reduce 24%
17/08/11 06:28:05 INFO mapreduce.Job:  map 100% reduce 26%
17/08/11 06:28:07 INFO mapreduce.Job:  map 100% reduce 27%
17/08/11 06:28:08 INFO mapreduce.Job:  map 100% reduce 28%
17/08/11 06:28:10 INFO mapreduce.Job:  map 100% reduce 34%
17/08/11 06:28:11 INFO mapreduce.Job:  map 100% reduce 40%
17/08/11 06:28:13 INFO mapreduce.Job:  map 100% reduce 43%
17/08/11 06:28:14 INFO mapreduce.Job:  map 100% reduce 49%
17/08/11 06:28:15 INFO mapreduce.Job:  map 100% reduce 50%
17/08/11 06:28:16 INFO mapreduce.Job:  map 100% reduce 55%
17/08/11 06:28:17 INFO mapreduce.Job:  map 100% reduce 56%
17/08/11 06:28:19 INFO mapreduce.Job:  map 100% reduce 57%
17/08/11 06:28:20 INFO mapreduce.Job:  map 100% reduce 58%
17/08/11 06:28:23 INFO mapreduce.Job:  map 100% reduce 61%
17/08/11 06:28:26 INFO mapreduce.Job:  map 100% reduce 62%
17/08/11 06:28:27 INFO mapreduce.Job:  map 100% reduce 63%
17/08/11 06:28:36 INFO mapreduce.Job:  map 100% reduce 67%
17/08/11 06:28:42 INFO mapreduce.Job:  map 100% reduce 71%
17/08/11 06:28:45 INFO mapreduce.Job:  map 100% reduce 72%
17/08/11 06:28:48 INFO mapreduce.Job:  map 100% reduce 74%
17/08/11 06:28:51 INFO mapreduce.Job:  map 100% reduce 75%
17/08/11 06:28:59 INFO mapreduce.Job:  map 100% reduce 79%
17/08/11 06:29:02 INFO mapreduce.Job:  map 100% reduce 81%
17/08/11 06:29:05 INFO mapreduce.Job:  map 100% reduce 84%
17/08/11 06:29:08 INFO mapreduce.Job:  map 100% reduce 85%
17/08/11 06:29:09 INFO mapreduce.Job:  map 100% reduce 89%
17/08/11 06:29:11 INFO mapreduce.Job:  map 100% reduce 90%
17/08/11 06:29:12 INFO mapreduce.Job:  map 100% reduce 93%
17/08/11 06:29:14 INFO mapreduce.Job:  map 100% reduce 94%
17/08/11 06:29:15 INFO mapreduce.Job:  map 100% reduce 96%
17/08/11 06:29:18 INFO mapreduce.Job:  map 100% reduce 97%
17/08/11 06:29:21 INFO mapreduce.Job:  map 100% reduce 98%
17/08/11 06:29:25 INFO mapreduce.Job:  map 100% reduce 99%
17/08/11 06:29:27 INFO mapreduce.Job:  map 100% reduce 100%
17/08/11 06:29:28 INFO mapreduce.Job: Job job_1502446388515_0003 completed successfully
17/08/11 06:29:28 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=2933917001
		FILE: Number of bytes written=5822044614
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=6553616800
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=360
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters
		Launched map tasks=112
		Launched reduce tasks=8
		Data-local map tasks=112
		Total time spent by all maps in occupied slots (ms)=747740
		Total time spent by all reduces in occupied slots (ms)=254305
		Total time spent by all map tasks (ms)=747740
		Total time spent by all reduce tasks (ms)=254305
		Total vcore-seconds taken by all map tasks=747740
		Total vcore-seconds taken by all reduce tasks=254305
		Total megabyte-seconds taken by all map tasks=765685760
		Total megabyte-seconds taken by all reduce tasks=260408320
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Map output bytes=6684672000
		Map output materialized bytes=2873034227
		Input split bytes=16800
		Combine input records=0
		Combine output records=0
		Reduce input groups=65536000
		Reduce shuffle bytes=2873034227
		Reduce input records=65536000
		Reduce output records=65536000
		Spilled Records=131072000
		Shuffled Maps =896
		Failed Shuffles=0
		Merged Map outputs=896
		GC time elapsed (ms)=12576
		CPU time spent (ms)=678470
		Physical memory (bytes) snapshot=62411014144
		Virtual memory (bytes) snapshot=188718129152
		Total committed heap usage (bytes)=69311397888
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
17/08/11 06:29:28 INFO terasort.TeraSort: done
```

time
```
real	4m20.776s
user	0m8.742s
sys	0m0.367s
```
