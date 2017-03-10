### Cloud Provider used
* AWS

### Node IPs and hostnames
```
ifconfig
hostname
```
* ip-172-31-20-21.eu-central-1.compute.internal (172.31.20.21)
* ip-172-31-23-106.eu-central-1.compute.internal (172.31.23.106)
* ip-172-31-20-100.eu-central-1.compute.internal (172.31.20.100)
* ip-172-31-19-63.eu-central-1.compute.internal (172.31.19.63)
* ip-172-31-17-194.eu-central-1.compute.internal (172.31.17.194)

### Linux release
```
cat /etc/redhat-release
```
* Red Hat Enterprise Linux Server release 6.7 (Santiago)

### disk capacity available on each node is >= 30 GB
```
df -h /
```

* ip-172-31-20-21.eu-central-1.compute.internal
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.1G   26G   8% /
```

* ip-172-31-23-106.eu-central-1.compute.internal
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.1G   26G   8% /
```

* ip-172-31-20-100.eu-central-1.compute.internal
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.1G   26G   8% /
```

* ip-172-31-19-63.eu-central-1.compute.internal
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.1G   26G   8% /
```

* ip-172-31-17-194.eu-central-1.compute.internal
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.1G   26G   8% /
```

### yum repolist enabled
```
[root@ip-172-31-20-21 ec2-user]# yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                             repo name                                                                                                         status
rhui-REGION-client-config-server-6                                                  Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                       3
rhui-REGION-rhel-server-releases                                                    Red Hat Enterprise Linux Server 6 (RPMs)                                                                          18558
rhui-REGION-rhel-server-rh-common                                                   Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                  129
repolist: 18690

[root@ip-172-31-23-106 ec2-user]# yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                             repo name                                                                                                         status
rhui-REGION-client-config-server-6                                                  Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                       3
rhui-REGION-rhel-server-releases                                                    Red Hat Enterprise Linux Server 6 (RPMs)                                                                          18558
rhui-REGION-rhel-server-rh-common                                                   Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                  129
repolist: 18690

[root@ip-172-31-20-100 ec2-user]# yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                             repo name                                                                                                         status
rhui-REGION-client-config-server-6                                                  Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                       3
rhui-REGION-rhel-server-releases                                                    Red Hat Enterprise Linux Server 6 (RPMs)                                                                          18558
rhui-REGION-rhel-server-rh-common                                                   Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                  129
repolist: 18690

[root@ip-172-31-19-63 ec2-user]# yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                             repo name                                                                                                         status
rhui-REGION-client-config-server-6                                                  Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                       3
rhui-REGION-rhel-server-releases                                                    Red Hat Enterprise Linux Server 6 (RPMs)                                                                          18558
rhui-REGION-rhel-server-rh-common                                                   Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                  129
repolist: 18690

[root@ip-172-31-17-194 ec2-user]# yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                             repo name                                                                                                         status
rhui-REGION-client-config-server-6                                                  Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                       3
rhui-REGION-rhel-server-releases                                                    Red Hat Enterprise Linux Server 6 (RPMs)                                                                          18558
rhui-REGION-rhel-server-rh-common                                                   Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                  129
repolist: 18690
```

### adding users-> groups ronaldo->barca and neymar->merengues
```
[root@ip-172-31-20-21 ec2-user]# cat /etc/passwd | grep ronaldo
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
[root@ip-172-31-20-21 ec2-user]# cat /etc/passwd | grep neymar
neymar:x:2010:2010::/home/neymar:/bin/bash
[root@ip-172-31-20-21 ec2-user]# cat /etc/group | grep barca
barca:x:3016:ronaldo
[root@ip-172-31-20-21 ec2-user]# cat /etc/group | grep merengues
merengues:x:3010:neymar
```
