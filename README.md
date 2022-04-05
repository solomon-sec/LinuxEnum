# LinuxEnum
Welcome to the Linux Commands for Local Enumeration Cheat Sheet


## Summary

* [User Enumeration](#userenumeration)
* [Operating System](#operatingsystem)
* [Networking](#network)
* [Services](#services)
* [Environment Variables](#environmentvar)






## User Enumeration

```bash
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

```bash
uname -a
lsb_release -a
cat /etc/issue  
cat /proc/version
cat /etc/*-release
dmesg | grep linux 
```


## Networking

```bash
arp -a
ip addr
ip link
ifconfig
hostname
route -n
iptables -L
netstat -anotp
cat /etc/networks 

```
## Services

```bash
ps
top
ps aux
ps auxwww
ps -u root
ps -u $USER
cat /etc/services
ps aux | grep root
```

## Environment variables

```bash
env
set
cat ~/.zshrc
cat ~/.bashrc
cat /etc/profile
cat ~/.bash_logout 
cat /etc/bash.bashrc
```
