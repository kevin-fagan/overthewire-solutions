# Level 8

### Instructions
The password for the next level is stored in the file data.txt next to the word millionth

### Solutions
1. Ensure you are logged in as `bandit7`:
```
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

1. We can use the `grep` command to find the line that contains the password we are looking for:
```shell
bandit7@bandit:~$ grep "millionth" data.txt 
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```