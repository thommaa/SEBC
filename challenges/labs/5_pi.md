
```bash
sudo su - igneous
kinit igneous
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 50 100
```

output
```
[igneous@ip-172-31-21-32 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 50 100
Number of Maps  = 50
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Wrote input for Map #10
Wrote input for Map #11
Wrote input for Map #12
Wrote input for Map #13
Wrote input for Map #14
Wrote input for Map #15
Wrote input for Map #16
Wrote input for Map #17
Wrote input for Map #18
Wrote input for Map #19
Wrote input for Map #20
Wrote input for Map #21
Wrote input for Map #22
Wrote input for Map #23
Wrote input for Map #24
Wrote input for Map #25
Wrote input for Map #26
Wrote input for Map #27
Wrote input for Map #28
Wrote input for Map #29
Wrote input for Map #30
Wrote input for Map #31
Wrote input for Map #32
Wrote input for Map #33
Wrote input for Map #34
Wrote input for Map #35
Wrote input for Map #36
Wrote input for Map #37
Wrote input for Map #38
Wrote input for Map #39
Wrote input for Map #40
Wrote input for Map #41
Wrote input for Map #42
Wrote input for Map #43
Wrote input for Map #44
Wrote input for Map #45
Wrote input for Map #46
Wrote input for Map #47
Wrote input for Map #48
Wrote input for Map #49
Starting Job
17/08/11 06:27:55 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-175.eu-west-1.compute.internal/172.31.21.175:8032
17/08/11 06:27:55 INFO hdfs.DFSClient: Created token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447275941, maxDate=1503052075941, sequenceNumber=4, masterKeyId=2 on 172.31.21.175:8020
17/08/11 06:27:55 INFO security.TokenCache: Got dt for hdfs://ip-172-31-21-175.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447275941, maxDate=1503052075941, sequenceNumber=4, masterKeyId=2)
17/08/11 06:27:56 INFO input.FileInputFormat: Total input paths to process : 50
17/08/11 06:27:56 INFO mapreduce.JobSubmitter: number of splits:50
17/08/11 06:27:56 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502446388515_0004
17/08/11 06:27:56 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for igneous: HDFS_DELEGATION_TOKEN owner=igneous@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502447275941, maxDate=1503052075941, sequenceNumber=4, masterKeyId=2)
17/08/11 06:27:56 INFO impl.YarnClientImpl: Submitted application application_1502446388515_0004
17/08/11 06:27:56 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-175.eu-west-1.compute.internal:8088/proxy/application_1502446388515_0004/
17/08/11 06:27:56 INFO mapreduce.Job: Running job: job_1502446388515_0004
17/08/11 06:28:07 INFO mapreduce.Job: Job job_1502446388515_0004 running in uber mode : false
17/08/11 06:28:07 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 06:28:25 INFO mapreduce.Job:  map 4% reduce 0%
17/08/11 06:28:26 INFO mapreduce.Job:  map 6% reduce 0%
17/08/11 06:28:31 INFO mapreduce.Job:  map 12% reduce 0%
17/08/11 06:28:33 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 06:28:36 INFO mapreduce.Job:  map 18% reduce 0%
17/08/11 06:28:37 INFO mapreduce.Job:  map 20% reduce 0%
17/08/11 06:28:38 INFO mapreduce.Job:  map 22% reduce 0%
17/08/11 06:28:40 INFO mapreduce.Job:  map 24% reduce 0%
17/08/11 06:28:41 INFO mapreduce.Job:  map 26% reduce 0%
17/08/11 06:28:42 INFO mapreduce.Job:  map 28% reduce 0%
17/08/11 06:28:43 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 06:28:44 INFO mapreduce.Job:  map 32% reduce 0%
17/08/11 06:28:47 INFO mapreduce.Job:  map 34% reduce 0%
17/08/11 06:28:48 INFO mapreduce.Job:  map 40% reduce 0%
17/08/11 06:28:52 INFO mapreduce.Job:  map 42% reduce 0%
17/08/11 06:28:53 INFO mapreduce.Job:  map 44% reduce 0%
17/08/11 06:28:54 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 06:28:56 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 06:28:58 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 06:28:59 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 06:29:00 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 06:29:04 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 06:29:06 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 06:29:09 INFO mapreduce.Job:  map 64% reduce 0%
17/08/11 06:29:10 INFO mapreduce.Job:  map 68% reduce 0%
17/08/11 06:29:14 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 06:29:15 INFO mapreduce.Job:  map 74% reduce 0%
17/08/11 06:29:18 INFO mapreduce.Job:  map 76% reduce 0%
17/08/11 06:29:19 INFO mapreduce.Job:  map 78% reduce 0%
17/08/11 06:29:20 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 06:29:21 INFO mapreduce.Job:  map 82% reduce 0%
17/08/11 06:29:22 INFO mapreduce.Job:  map 84% reduce 0%
17/08/11 06:29:25 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 06:29:26 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 06:29:27 INFO mapreduce.Job:  map 92% reduce 0%
17/08/11 06:29:30 INFO mapreduce.Job:  map 94% reduce 0%
17/08/11 06:29:32 INFO mapreduce.Job:  map 98% reduce 0%
17/08/11 06:29:33 INFO mapreduce.Job:  map 100% reduce 100%
17/08/11 06:29:34 INFO mapreduce.Job: Job job_1502446388515_0004 completed successfully
17/08/11 06:29:34 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=258
		FILE: Number of bytes written=6376280
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=15040
		HDFS: Number of bytes written=215
		HDFS: Number of read operations=203
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Job Counters
		Launched map tasks=50
		Launched reduce tasks=1
		Data-local map tasks=49
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=226735
		Total time spent by all reduces in occupied slots (ms)=6626
		Total time spent by all map tasks (ms)=226735
		Total time spent by all reduce tasks (ms)=6626
		Total vcore-seconds taken by all map tasks=226735
		Total vcore-seconds taken by all reduce tasks=6626
		Total megabyte-seconds taken by all map tasks=232176640
		Total megabyte-seconds taken by all reduce tasks=6785024
	Map-Reduce Framework
		Map input records=50
		Map output records=100
		Map output bytes=900
		Map output materialized bytes=1700
		Input split bytes=9140
		Combine input records=0
		Combine output records=0
		Reduce input groups=2
		Reduce shuffle bytes=1700
		Reduce input records=100
		Reduce output records=0
		Spilled Records=200
		Shuffled Maps =50
		Failed Shuffles=0
		Merged Map outputs=50
		GC time elapsed (ms)=1679
		CPU time spent (ms)=32320
		Physical memory (bytes) snapshot=22593163264
		Virtual memory (bytes) snapshot=80206114816
		Total committed heap usage (bytes)=25782910976
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=5900
	File Output Format Counters
		Bytes Written=97
Job Finished in 99.179 seconds
Estimated value of Pi is 3.14160000000000000000
```
