# Level 7

### Instructions
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size



### Solutions
1. Ensure you are logged in as `bandit6`:
   <br>
    ```
    ssh bandit6@bandit.labs.overthewire.org -p 2220
    ```
2. We can use the `find` command to find the file we are looking for:
    <br>
    ```shell
    bandit6@bandit:/$ find . -user bandit7 -size 33c -group bandit6
    find: ‘./etc/ssl/private’: Permission denied
    find: ‘./etc/polkit-1/localauthority’: Permission denied
    find: ‘./etc/sudoers.d’: Permission denied
    .
    .
    .
    ./var/lib/dpkg/info/bandit7.password
    .
    .
    .
    bandit6@bandit:/$ cat ./var/lib/dpkg/info/bandit7.password
    z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

    ```