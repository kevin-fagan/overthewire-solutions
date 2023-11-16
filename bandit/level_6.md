# Level 6

### Instructions
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable


### Solutions
1. Ensure you are logged in as `bandit5`:
   <br>
    ```
    ssh bandit5@bandit.labs.overthewire.org -p 2220
    ```
2. We can use the `find` command to find the file we are looking for. We want to find a file that is not exectuable and is 1033 bits in size. We can do so like such:
   <br>
   ```shell
   bandit5@bandit:~$ find ./inhere/ -not -executable -size 1033c
   ./inhere/maybehere07/.file2
   bandit5@bandit:~$ cat ./inhere/maybehere07/.file2
   P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
   ```