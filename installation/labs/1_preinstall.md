## preinstall check steps (do for all nodes!)

### checking rhel version 
* cat /etc/redhat-release

### checking and adjusting swappiness
* echo "vm.swappiness = 1" >> /etc/sysctl.conf
* echo 1 > /proc/sys/vm/swappiness

### showing the mount attributes of all volumes
* cat /etc/fstab

### showing the reserve space of non-root volumes
* df –h /

### check and disable iptables. Firewall between nodes can cause really silly failures
* /sbin/chkconfig --list iptables
* /sbin/chkconfig --list ip6tables
* /sbin/chkconfig iptables off
* /sbin/chkconfig ip6tables off

### check and deactivate SELinux. Might need to restart node
* selinuxenabled || echo "disabled"
* cat /etc/sysconfig/selinux 

### deactiveate not used services
* service cups stop && chkconfig cups off
* service postfix stop && chkconfig postfix off

### check ulimits for role users
* echo hdfs - nofile 32768 >> /etc/security/limits.conf
* echo mapred - nofile 32768 >> /etc/security/limits.conf
* echo hbase - nofile 32768 >> /etc/security/limits.conf
* echo hdfs - nproc 32768 >> /etc/security/limits.conf
* echo mapred - nproc 32768 >> /etc/security/limits.conf
* echo hbase - nproc 32768 >> /etc/security/limits.conf

### deactivate transparent huge pages
* echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag

### list network interface configuration
* cat /etc/sysconfig/network-scripts/ifcfg-eth0

### list forward and reverse host lookup
* nslookup `hostname`
* nslookup 172.31.26.85 (use ip returned through nslookup)

### check ntp service is running
* service ntpd status
* service ntpd start (start, if not running)
* yum install nscd (install, if not installed)

### check nscd ist running
* service nscd status
* service nscd start (start, if not running)
* yum install nscd (install, if not installed)



