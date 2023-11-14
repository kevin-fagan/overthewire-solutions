# Level 2

### Instructions
The password for the next level is stored in a file called - located in the home directory

### Solution

1. Ensure you are logged in as `bandit1`:
   
```shell
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

2. Using "-" as a filename is entirely valid. However, it can cause confusion as command options typically begin with a dash. Therefore, if you try to use `cat -`, the output may not be as anticipated. This issue can be resolved by specifying the file's path like such:
```shell
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

