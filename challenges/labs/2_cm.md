# List the command and output
```
[root@ip-172-31-28-142 ~]# ls /etc/yum.repos.d
cloudera-manager.repo  mysql-community-source.repo     redhat-rhui.repo          rhel-source.repo
mysql-community.repo   redhat-rhui-client-config.repo  redhat-rhui.repo.rpmsave  rhui-load-balancers.conf
```

# Connect Cloudera Manager to the database
```
/usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-23-52.eu-west-1.compute.internal -P 3306 -u temp -p --scm-host ip-172-31-28-142.eu-west-1.compute.internal cmf cmf cmf
```
Result
```
[root@ip-172-31-28-142 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-23-52.eu-west-1.compute.internal -P 3306 -u temp -p --scm-host ip-172-31-28-142.eu-west-1.compute.internal cmf cmf cmf
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2017-08-11 04:30:57,145] INFO     0[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java) - Successfully connected to database.
All done, your SCM database is configured correctly!
```
