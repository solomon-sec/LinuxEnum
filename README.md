# LinuxEnum
Welcome to the Linux Commands for Local Enumeration Cheat Sheet


## Summary

* [User Enumeration](#userenumeration)






## User Enumeration
```sh
whoami
uname -a
groups
id $whoami
groups $whoami
for user in $(awk -F ':' '{print $1}' /etc/passwd); do finger $user;done |grep Shell  2>/dev/null
```
