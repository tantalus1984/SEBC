### add tantalus1984 to sentry admins in CM
* add "tantalus1984" to "sentry.service.admin.group"

### start beeline
* beeline
* !connect jdbc:hive2://ip-172-31-27-141.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-27-141.eu-central-1.compute.internal@EXAMPLE.COM

### create sentry_admin role
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170308110505_6b5f5adf-cd30-4aa2-a25f-e4b4f7127e3e): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308110505_6b5f5adf-cd30-4aa2-a25f-e4b4f7127e3e); Time taken: 0.065 seconds
INFO  : Executing command(queryId=hive_20170308110505_6b5f5adf-cd30-4aa2-a25f-e4b4f7127e3e): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308110505_6b5f5adf-cd30-4aa2-a25f-e4b4f7127e3e); Time taken: 0.577 seconds
INFO  : OK
No rows affected (0.651 seconds)
```

### grant all privileges to sentry_admin role on server1
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170308110606_974e01b1-f72f-478b-80a9-ad48c978058a): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308110606_974e01b1-f72f-478b-80a9-ad48c978058a); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20170308110606_974e01b1-f72f-478b-80a9-ad48c978058a): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308110606_974e01b1-f72f-478b-80a9-ad48c978058a); Time taken: 0.098 seconds
INFO  : OK
No rows affected (0.174 seconds)
```

### grant sentry_admin role to tantalus1984's group
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT ROLE sentry_admin TO GROUP tantalus194;
INFO  : Compiling command(queryId=hive_20170308110707_a8d94ac6-e9e2-47a4-8b39-bda0ab2af43b): GRANT ROLE sentry_admin TO GROUP tantalus194
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308110707_a8d94ac6-e9e2-47a4-8b39-bda0ab2af43b); Time taken: 0.052 seconds
INFO  : Executing command(queryId=hive_20170308110707_a8d94ac6-e9e2-47a4-8b39-bda0ab2af43b): GRANT ROLE sentry_admin TO GROUP tantalus194
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308110707_a8d94ac6-e9e2-47a4-8b39-bda0ab2af43b); Time taken: 0.082 seconds
INFO  : OK
No rows affected (0.142 seconds)
```

### show tables
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20170308112121_5fefa57d-b4f3-4c55-a605-e054a3bd26f0): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308112121_5fefa57d-b4f3-4c55-a605-e054a3bd26f0); Time taken: 0.05 seconds
INFO  : Executing command(queryId=hive_20170308112121_5fefa57d-b4f3-4c55-a605-e054a3bd26f0): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308112121_5fefa57d-b4f3-4c55-a605-e054a3bd26f0); Time taken: 0.121 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.209 seconds)
```

### creating new users and groups
```
groupadd selector
groupadd inserters
useradd -u 1100 -g selector george
useradd -u 1200 -g inserters ferdinand

### change password for george and ferdinand
* passwd george
* passwd ferdinand

### add kerperos principals
```
kadmin.local -q "addprinc -randkey george"
kadmin.local -q "change_password -pw cloudera george"
kadmin.local -q "addprinc -randkey ferdinand"
kadmin.local -q "change_password -pw cloudera ferdinand"
```

### create reads role
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20170308112929_e7106330-d821-4f77-a48e-00c45aaa1fdd): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308112929_e7106330-d821-4f77-a48e-00c45aaa1fdd); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20170308112929_e7106330-d821-4f77-a48e-00c45aaa1fdd): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308112929_e7106330-d821-4f77-a48e-00c45aaa1fdd); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.139 seconds)
```

### create writes role
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20170308113030_b6e26a70-18a8-4ba1-9555-0c8dcb50be90): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113030_b6e26a70-18a8-4ba1-9555-0c8dcb50be90); Time taken: 0.048 seconds
INFO  : Executing command(queryId=hive_20170308113030_b6e26a70-18a8-4ba1-9555-0c8dcb50be90): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113030_b6e26a70-18a8-4ba1-9555-0c8dcb50be90); Time taken: 0.024 seconds
INFO  : OK
No rows affected (0.079 seconds)
```

### Grant read privilege for all tables to reads
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20170308113030_0c7f17e5-f492-47a9-a3ea-8a3a18243bb0): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113030_0c7f17e5-f492-47a9-a3ea-8a3a18243bb0); Time taken: 0.055 seconds
INFO  : Executing command(queryId=hive_20170308113030_0c7f17e5-f492-47a9-a3ea-8a3a18243bb0): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113030_0c7f17e5-f492-47a9-a3ea-8a3a18243bb0); Time taken: 0.031 seconds
INFO  : OK
No rows affected (0.093 seconds)

0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20170308113131_d1fe8140-c7f0-48ed-844c-c13963bb7188): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113131_d1fe8140-c7f0-48ed-844c-c13963bb7188); Time taken: 0.049 seconds
INFO  : Executing command(queryId=hive_20170308113131_d1fe8140-c7f0-48ed-844c-c13963bb7188): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113131_d1fe8140-c7f0-48ed-844c-c13963bb7188); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.086 seconds)
```

### Grant read privilege for default.sample07 only to 'writes'
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20170308113333_f39d1fb2-e238-48df-bda9-1e01f520d299): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113333_f39d1fb2-e238-48df-bda9-1e01f520d299); Time taken: 0.048 seconds
INFO  : Executing command(queryId=hive_20170308113333_f39d1fb2-e238-48df-bda9-1e01f520d299): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113333_f39d1fb2-e238-48df-bda9-1e01f520d299); Time taken: 0.085 seconds
INFO  : OK
No rows affected (0.142 seconds)

0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20170308113434_3aa81f2c-9c8c-4090-a773-34603d488059): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113434_3aa81f2c-9c8c-4090-a773-34603d488059); Time taken: 0.088 seconds
INFO  : Executing command(queryId=hive_20170308113434_3aa81f2c-9c8c-4090-a773-34603d488059): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113434_3aa81f2c-9c8c-4090-a773-34603d488059); Time taken: 0.046 seconds
INFO  : OK
No rows affected (0.142 seconds)

0: jdbc:hive2://ip-172-31-27-141.eu-central-1> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20170308113434_03152eef-026b-4337-8569-ee9c8acb808b): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113434_03152eef-026b-4337-8569-ee9c8acb808b); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20170308113434_03152eef-026b-4337-8569-ee9c8acb808b): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113434_03152eef-026b-4337-8569-ee9c8acb808b); Time taken: 0.033 seconds
INFO  : OK
No rows affected (0.094 seconds)
```

### kinit as george, then login to beeline and show tables;
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20170308113939_477f3c4f-78b4-4e66-a519-678dd92c0764): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308113939_477f3c4f-78b4-4e66-a519-678dd92c0764); Time taken: 0.057 seconds
INFO  : Executing command(queryId=hive_20170308113939_477f3c4f-78b4-4e66-a519-678dd92c0764): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308113939_477f3c4f-78b4-4e66-a519-678dd92c0764); Time taken: 0.113 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.301 seconds)
```

### kinit as george, then login to beeline and show tables;
```
0: jdbc:hive2://ip-172-31-27-141.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20170308114040_bbf1830c-cffd-4802-a1d0-92064ecba1a4): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308114040_bbf1830c-cffd-4802-a1d0-92064ecba1a4); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20170308114040_bbf1830c-cffd-4802-a1d0-92064ecba1a4): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308114040_bbf1830c-cffd-4802-a1d0-92064ecba1a4); Time taken: 0.115 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.305 seconds)
```
