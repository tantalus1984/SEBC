### Report the latest available version of the API
* http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/version
```v14```

### Report the CM version
* http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v13/cm/version
```{
  "version" : "5.9.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170112-1158",
  "gitHash" : "a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1",
  "snapshot" : false
}```

### List all CM users
* http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v13/users
```{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  }, {
    "name" : "tantalus1984",
    "roles" : [ "ROLE_ADMIN" ]
  } ]
}```

### Report the database server in use by CM
* http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo
```{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
