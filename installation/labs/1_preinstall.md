## preinstall check steps (do for all nodes!)

### checking rhel version 
*cat /etc/redhat-release

### checking and adjusting swappiness
*echo "vm.swappiness = 1" >> /etc/sysctl.conf
*echo 1 > /proc/sys/vm/swappiness

### check NTP. All nodes must have the same time
*grep server /etc/ntp.conf

### check and disable iptables. Firewall between nodes can cause really silly failures
*/sbin/chkconfig --list iptables
*/sbin/chkconfig --list ip6tables
*/sbin/chkconfig iptables off
*/sbin/chkconfig ip6tables off

### check and deactivate SELinux. Might need to restart node
*selinuxenabled || echo "disabled"
*cat /etc/sysconfig/selinux 

### deactiveate not used services
*service cups stop && chkconfig cups off
*service postfix stop && chkconfig postfix off

### check ulimits for role users
*echo hdfs - nofile 32768 >> /etc/security/limits.conf
*echo mapred - nofile 32768 >> /etc/security/limits.conf
*echo hbase - nofile 32768 >> /etc/security/limits.conf
*echo hdfs - nproc 32768 >> /etc/security/limits.conf
*echo mapred - nproc 32768 >> /etc/security/limits.conf
*echo hbase - nproc 32768 >> /etc/security/limits.conf

### deactivate transparent huge pages
*echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag

### check no java is installed yet
*echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag

### check Python is working and version 2.6
*python




