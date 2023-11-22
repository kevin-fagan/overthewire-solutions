# Level 18

### Instructions
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

### Solutions
1. Ensure you are logged in as `bandit17`:
```
ssh bandit17@bandit.labs.overthewire.org -p 2220
```

2. We can use the `diff` command to figure out the line that differs betweent the two files:
``` shell
bandit17@bandit:~$ diff passwords.new passwords.old 
42c42
< hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
---
> p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
```