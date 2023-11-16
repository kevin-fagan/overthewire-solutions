# Level 4

### Instructions
The password for the next level is stored in a hidden file in the inhere directory.

### Solutions
1. Ensure you are logged in as `bandit3`:
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

2. The password for the next level is stored within `~/inhere/.hidden`. Hidden files always begin with a `.` and may not appear when using commands such as `ls`. However, you can use `ls -a` to show ALL files, including ones that are hidden.
```shell
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```