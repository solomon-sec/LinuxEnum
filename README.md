# LinuxEnum
Welcome to the Linux Commands for Local Enumeration Cheat Sheet


## Summary

* [User Enumeration](#userenumeration)
* [Operating System](#operatingsystem)
* [Networking](#network)






## User Enumeration
```sh
finger
whoami
uname -a
groups
id $whoami
groups $whoami
cat /etc/group
cat /etc/passwd
for user in $(awk -F ':' '{print $1}' /etc/passwd); do finger $user;done |grep Shell  2>/dev/null
```

## Operating System
```sh
uname -a
lsb_release -a
cat /etc/issue  
cat /proc/version
cat /etc/*-release
dmesg | grep linux 
```


## Networking
```sh
ifconfig
ip addr
ip link
cat /etc/networks 
hostname
netstat -anotp
iptables -L
arp -a
route -n
```



```
