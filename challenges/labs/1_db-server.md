# MySQL server installation:

# Hostname:
```
[root@ip-172-31-23-52 ~]# hostname
ip-172-31-23-52.eu-west-1.compute.internal
```

# MySQL version
```
[root@ip-172-31-23-52 ~]# mysqld --version
mysqld  Ver 5.5.57 for Linux on x86_64 (MySQL Community Server (GPL))
```

# Show DB content
```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
8 rows in set (0.00 sec)
```
