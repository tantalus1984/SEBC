### yum repository listing
```
[root@ip-172-31-23-106 yum.repos.d]# ls /etc/yum.repos.d/
cloudera.repo  mysql.repo  redhat-rhui-client-config.repo  redhat-rhui.repo  redhat.repo  rhel-source.repo  rhui-load-balancers.conf
```

### running scm_prepare_database.sh
```
[root@ip-172-31-23-106 yum.repos.d]# /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm_password -h ip-172-31-20-21.eu-central-1.compute.internal -P 3306 —scm-host ip-172-31-23-106.eu-central-1.compute.internal
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2017-03-10 03:52:46,632] INFO     0[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java) - Successfully connected to database.
All done, your SCM database is configured correctly!
```
