* As user nimbus, use teragen to generate a 65,536,000-record dataset
```bash
sudo su - nimbus
HDexample=/opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
time hadoop jar ${HDexample}/hadoop-mapreduce-examples.jar teragen \
             -Dmapreduce.job.maps=16 \
             -Ddfs.block.size=67108864 \
             -Dmapreduce.map.memory.mb=768 \
             655360 /user/nimbus/tgen

```

teragen output
```
17/08/11 05:54:06 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-175.eu-west-1.compute.internal/172.31.21.175:8032
17/08/11 05:54:07 INFO terasort.TeraSort: Generating 655360 using 16
17/08/11 05:54:07 INFO mapreduce.JobSubmitter: number of splits:16
17/08/11 05:54:07 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/08/11 05:54:07 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502443689266_0001
17/08/11 05:54:08 INFO impl.YarnClientImpl: Submitted application application_1502443689266_0001
17/08/11 05:54:08 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-175.eu-west-1.compute.internal:8088/proxy/application_1502443689266_0001/
17/08/11 05:54:08 INFO mapreduce.Job: Running job: job_1502443689266_0001
17/08/11 05:54:14 INFO mapreduce.Job: Job job_1502443689266_0001 running in uber mode : false
17/08/11 05:54:14 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 05:54:21 INFO mapreduce.Job:  map 6% reduce 0%
17/08/11 05:54:23 INFO mapreduce.Job:  map 19% reduce 0%
17/08/11 05:54:25 INFO mapreduce.Job:  map 38% reduce 0%
17/08/11 05:54:26 INFO mapreduce.Job:  map 44% reduce 0%
17/08/11 05:54:28 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 05:54:29 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 05:54:31 INFO mapreduce.Job:  map 63% reduce 0%
17/08/11 05:54:32 INFO mapreduce.Job:  map 69% reduce 0%
17/08/11 05:54:33 INFO mapreduce.Job:  map 81% reduce 0%
17/08/11 05:54:34 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 05:54:35 INFO mapreduce.Job:  map 94% reduce 0%
17/08/11 05:54:36 INFO mapreduce.Job:  map 100% reduce 0%
17/08/11 05:54:36 INFO mapreduce.Job: Job job_1502443689266_0001 completed successfully
17/08/11 05:54:36 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1976630
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1340
		HDFS: Number of bytes written=65536000
		HDFS: Number of read operations=64
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=32
	Job Counters
		Launched map tasks=16
		Other local map tasks=16
		Total time spent by all maps in occupied slots (ms)=93422
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=93422
		Total vcore-seconds taken by all map tasks=93422
		Total megabyte-seconds taken by all map tasks=95664128
	Map-Reduce Framework
		Map input records=655360
		Map output records=655360
		Input split bytes=1340
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=667
		CPU time spent (ms)=31660
		Physical memory (bytes) snapshot=3046080512
		Virtual memory (bytes) snapshot=21556649984
		Total committed heap usage (bytes)=3916431360
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=1408100361519672
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=65536000
```

time result
```
real	0m32.507s
user	0m5.650s
sys	0m0.309s

```

```
[nimbus@ip-172-31-23-52 ~]$ hdfs dfs -ls /user/nimbus/tgen
Found 17 items
-rw-r--r--   3 nimbus hdfs          0 2017-08-11 05:54 /user/nimbus/tgen/_SUCCESS
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00000
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00001
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00002
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00003
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00004
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00005
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00006
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00007
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00008
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00009
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00010
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00011
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00012
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00013
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00014
-rw-r--r--   3 nimbus hdfs    4096000 2017-08-11 05:54 /user/nimbus/tgen/part-m-00015
```

```
[nimbus@ip-172-31-23-52 ~]$ hadoop fsck -blocks /user/nimbus
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-21-175.eu-west-1.compute.internal:50070
FSCK started by nimbus (auth:SIMPLE) from /172.31.23.52 for path /user/nimbus at Fri Aug 11 05:56:05 EDT 2017
.................Status: HEALTHY
 Total size:	65536000 B
 Total dirs:	3
 Total files:	17
 Total symlinks:		0
 Total blocks (validated):	16 (avg. block size 4096000 B)
 Minimally replicated blocks:	16 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Fri Aug 11 05:56:05 EDT 2017 in 5 milliseconds


The filesystem under path '/user/nimbus' is HEALTHY
```
