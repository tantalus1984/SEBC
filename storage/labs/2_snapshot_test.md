### create precious directory in users home directory
* ```hdfs dfs -mkdir /user/tantalus1984/precious```
* ```hdfs dfs -chmod 700 /user/tantalus1984/precious```

### copy SEBC.zip to precious directory
* ```hdfs dfs -copyFromLocal SEBC.zip /user/tantalus1984/precious```

### make precious snapshottable
* ```export HADOOP_USER_NAME=hdfs``` (superuser privileges are required)
* ```hdfs dfsadmin -allowSnapshot /user/tantalus1984/precious```
* `(Allowing snaphot on /user/tantalus1984/precious succeeded)
* ```export HADOOP_USER_NAME=tantalus1984``` (change back to normal user)

### create a snapshot named sebc-hdfs-test
* ```hdfs dfs -createSnapshot /user/tantalus1984/precious sebc-hdfs-test```
* (Created snapshot /user/tantalus1984/precious/.snapshot/sebc-hdfs-test)

### delete SEBC.zip
* ```hdfs dfs -rm /user/tantalus1984/precious/SEBC.zip```
* ```hdfs dfs -ls /user/tantalus1984/precious/``` (ensure file is deleted)

### restore SEBC.zip
* ```hdfs dfs -cp /user/tantalus1984/precious/.snapshot/sebc-hdfs-test/SEBC.zip /user/tantalus1984/precious```
* ```hdfs dfs -ls /user/tantalus1984/precious/``` (ensure file is restored)
