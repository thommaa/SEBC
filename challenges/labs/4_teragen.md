* As user nimbus, use teragen to generate a 65,536,000-record dataset
```bash
sudo su - nimbus
HDexample=/opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
time hadoop jar ${HDexample}/hadoop-mapreduce-examples.jar teragen \
             -Dmapreduce.job.maps=16 \
             -Ddfs.block.size=67108864 \
             -Dmapreduce.map.memory.mb=768 \
             65536000 /user/nimbus/tgen

```

teragen output
```
[nimbus@ip-172-31-23-52 ~]$ time hadoop jar ${HDexample}/hadoop-mapreduce-examples.jar teragen \
>              -Dmapreduce.job.maps=16 \
>              -Ddfs.block.size=67108864 \
>              -Dmapreduce.map.memory.mb=768 \
>              65536000 /user/nimbus/tgen
17/08/11 06:20:51 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-175.eu-west-1.compute.internal/172.31.21.175:8032
17/08/11 06:20:51 INFO hdfs.DFSClient: Created token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502446851906, maxDate=1503051651906, sequenceNumber=2, masterKeyId=2 on 172.31.21.175:8020
17/08/11 06:20:51 INFO security.TokenCache: Got dt for hdfs://ip-172-31-21-175.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502446851906, maxDate=1503051651906, sequenceNumber=2, masterKeyId=2)
17/08/11 06:20:52 INFO terasort.TeraSort: Generating 65536000 using 16
17/08/11 06:20:52 INFO mapreduce.JobSubmitter: number of splits:16
17/08/11 06:20:52 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/08/11 06:20:52 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502446388515_0002
17/08/11 06:20:52 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.175:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@THOMMAA.PA, renewer=yarn, realUser=, issueDate=1502446851906, maxDate=1503051651906, sequenceNumber=2, masterKeyId=2)
17/08/11 06:20:52 INFO impl.YarnClientImpl: Submitted application application_1502446388515_0002
17/08/11 06:20:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-175.eu-west-1.compute.internal:8088/proxy/application_1502446388515_0002/
17/08/11 06:20:52 INFO mapreduce.Job: Running job: job_1502446388515_0002
17/08/11 06:21:02 INFO mapreduce.Job: Job job_1502446388515_0002 running in uber mode : false
17/08/11 06:21:02 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 06:21:16 INFO mapreduce.Job:  map 5% reduce 0%
17/08/11 06:21:17 INFO mapreduce.Job:  map 6% reduce 0%
17/08/11 06:21:18 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 06:21:21 INFO mapreduce.Job:  map 21% reduce 0%
17/08/11 06:21:22 INFO mapreduce.Job:  map 25% reduce 0%
17/08/11 06:21:24 INFO mapreduce.Job:  map 27% reduce 0%
17/08/11 06:21:25 INFO mapreduce.Job:  map 29% reduce 0%
17/08/11 06:21:27 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 06:21:28 INFO mapreduce.Job:  map 32% reduce 0%
17/08/11 06:21:29 INFO mapreduce.Job:  map 34% reduce 0%
17/08/11 06:21:30 INFO mapreduce.Job:  map 35% reduce 0%
17/08/11 06:21:31 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 06:21:32 INFO mapreduce.Job:  map 38% reduce 0%
17/08/11 06:21:33 INFO mapreduce.Job:  map 40% reduce 0%
17/08/11 06:21:34 INFO mapreduce.Job:  map 41% reduce 0%
17/08/11 06:21:35 INFO mapreduce.Job:  map 43% reduce 0%
17/08/11 06:21:36 INFO mapreduce.Job:  map 45% reduce 0%
17/08/11 06:21:37 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 06:21:38 INFO mapreduce.Job:  map 47% reduce 0%
17/08/11 06:21:39 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 06:21:40 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 06:21:41 INFO mapreduce.Job:  map 51% reduce 0%
17/08/11 06:21:42 INFO mapreduce.Job:  map 53% reduce 0%
17/08/11 06:21:43 INFO mapreduce.Job:  map 55% reduce 0%
17/08/11 06:21:44 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 06:21:49 INFO mapreduce.Job:  map 59% reduce 0%
17/08/11 06:21:50 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 06:21:51 INFO mapreduce.Job:  map 62% reduce 0%
17/08/11 06:21:52 INFO mapreduce.Job:  map 64% reduce 0%
17/08/11 06:21:53 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 06:21:54 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 06:21:55 INFO mapreduce.Job:  map 70% reduce 0%
17/08/11 06:21:56 INFO mapreduce.Job:  map 71% reduce 0%
17/08/11 06:21:58 INFO mapreduce.Job:  map 74% reduce 0%
17/08/11 06:21:59 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 06:22:02 INFO mapreduce.Job:  map 77% reduce 0%
17/08/11 06:22:03 INFO mapreduce.Job:  map 78% reduce 0%
17/08/11 06:22:05 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 06:22:06 INFO mapreduce.Job:  map 81% reduce 0%
17/08/11 06:22:08 INFO mapreduce.Job:  map 83% reduce 0%
17/08/11 06:22:09 INFO mapreduce.Job:  map 85% reduce 0%
17/08/11 06:22:11 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 06:22:12 INFO mapreduce.Job:  map 89% reduce 0%
17/08/11 06:22:14 INFO mapreduce.Job:  map 94% reduce 0%
17/08/11 06:22:20 INFO mapreduce.Job:  map 99% reduce 0%
17/08/11 06:22:22 INFO mapreduce.Job:  map 100% reduce 0%
17/08/11 06:22:22 INFO mapreduce.Job: Job job_1502446388515_0002 completed successfully
17/08/11 06:22:22 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1988550
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1368
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=64
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=32
	Job Counters
		Launched map tasks=16
		Other local map tasks=16
		Total time spent by all maps in occupied slots (ms)=411557
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=411557
		Total vcore-seconds taken by all map tasks=411557
		Total megabyte-seconds taken by all map tasks=421434368
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=1368
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2303
		CPU time spent (ms)=157600
		Physical memory (bytes) snapshot=4744728576
		Virtual memory (bytes) snapshot=21494677504
		Total committed heap usage (bytes)=5435293696
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=6553600000

```

time result
```
real	1m33.625s
user	0m6.075s
sys	0m0.313s

```

```
[nimbus@ip-172-31-23-52 ~]$ hdfs dfs -ls /user/nimbus/tgen
Found 17 items
-rw-r--r--   3 nimbus hdfs          0 2017-08-11 06:22 /user/nimbus/tgen/_SUCCESS
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00000
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00001
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00002
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00003
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00004
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00005
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00006
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00007
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:21 /user/nimbus/tgen/part-m-00008
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00009
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00010
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00011
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00012
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00013
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00014
-rw-r--r--   3 nimbus hdfs  409600000 2017-08-11 06:22 /user/nimbus/tgen/part-m-00015
```

```
[nimbus@ip-172-31-23-52 ~]$ hadoop fsck -blocks /user/nimbus
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-21-175.eu-west-1.compute.internal:50070
FSCK started by nimbus (auth:KERBEROS_SSL) from /172.31.23.52 for path /user/nimbus at Fri Aug 11 06:24:35 EDT 2017
...................
/user/nimbus/.Trash/Current/user/nimbus/tsort/_partition.lst:  Under replicated BP-2006689248-172.31.21.175-1502443635940:blk_1073742600_1776. Target Replicas is 10 but found 4 replica(s).
.........................Status: HEALTHY
 Total size:	6684672077 B
 Total dirs:	10
 Total files:	44
 Total symlinks:		0
 Total blocks (validated):	137 (avg. block size 48793226 B)
 Minimally replicated blocks:	137 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	1 (0.729927 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	2.890511
 Corrupt blocks:		0
 Missing replicas:		6 (1.4925373 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Fri Aug 11 06:24:35 EDT 2017 in 18 milliseconds


The filesystem under path '/user/nimbus' is HEALTHY
```
