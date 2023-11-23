# Level 10

### Instructions
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

### Solutions
1. Ensure you are logged in as `bandit9`:
```
ssh bandit9@bandit.labs.overthewire.org -p 2220
```
1. We can first use the `strings` command to get text that is considered "human readable". We can then pipe it over to `grep` to find any line that starts with `==`:
```shell
bandit9@bandit:~$ strings data.txt | grep ^==
========== passwordk^
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```