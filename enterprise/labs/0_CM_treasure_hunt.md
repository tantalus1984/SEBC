### What is ubertask optimization?
* Background: by default, map and reduce tasks are started within their own VM. This ensures that that the stability of one task does not affect the stability of other tasks. However, there is a certain cost associated with starting up a JVM for every task. This cost becomes significant when many small tasks are launched. MapReduce can optimize this situation by recycling the same JVM for every task. The Map/Reduce tasks are then run in one uber task.  
* in YARN set mapreduce.job.ubertask.enable=true

### Where in CM is the Kerberos Security Realm value displayed?
* in CM click "Administration -> Settings" and serach for "realm" to reveal the property "default_realm"

### Which CDH service(s) host a property for enabling Kerberos authentication?
* Kerberos is end-to-end and requires all Services to be kerberized
* HDFS, Hive, Hue, Oozie, Yarn, Zookeeper (HBase, Impala, Kafka, Solr, Sentry, Accumulo)

### How do you upgrade the CM agents?
* update the yum repository under /etc/yum.repos.d
* on a host with an agent run ```yum upgrade cloudera-manager-daemons cloudera-manager-agent```

### Give the tsquery statement used to chart Hue's CPU utilization?
* ```select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=hue```

### Name all the roles that make up the Hive service
* HiverServer2
* Hive Metastore Server
* Hive Gateway
* Hive WebHCat Server

### What steps must be completed before integrating Cloudera Manager with Kerberos?
* it is recommended to configure Lev-1 security, since CM will generate keytabs and push them down to the nodes via CM agents
* non-zero ticket lifetime and renewal lifetime should be supported by KDC
* create an OU and an admin principal within this OU in your KDC (e.g., AD)
* the admin princiapl is used by CM to generate the remaining service principals under the OU
* if AES-256 is used, make sure to roll out Java Cryptography Extensions (JCE) to all node's JREs
