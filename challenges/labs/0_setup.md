Prerequisites
?	Disable transparent Huge page (add the below lines to /etc/rc.local file)

echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled
echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag

?	Change VMswappiness

Open file /etc/sysctl.conf and add the line vm.swappiness = 10
Verify the same by listing contents of file /proc/sys/vm/swappiness

?	Disable firewall

chkconfig iptables off
chkconfig ip6tables off

?	Disable SELinux

Open the file /etc/selinux/config and disable SELINUX
?	Install NTP services and turn on ntpd service 

Yum –y install ntp
Chkconfig ntpd on
