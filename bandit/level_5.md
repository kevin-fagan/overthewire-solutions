# Level 5

### Instructions
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

### Solutions
1. Ensure you are logged in as `bandit4`:
```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

2. There are 10 files within the `inhere` directory. One of these files contains the password for the next level. We can `cat` each file one by one, or we can use the `file` command to determine which file is human readable:
```shell
bandit4@bandit:~/inhere$ file ./-file*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```
    
3. We can see that `-file07` contains `ASCII text`. We can `cat` this file to obtain the password:
    
```shell
bandit4@bandit:~/inhere$ cat ./-file07 
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```