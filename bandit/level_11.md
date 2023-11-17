# Level 11

### Instructions
The password for the next level is stored in the file data.txt, which contains base64 encoded data

### Solutions
1. Ensure you are logged in as `bandit10`:
```
ssh bandit10@bandit.labs.overthewire.org -p 2220
```
2. We can use the `base64` command to decode the contents of the file:
```shell
bandit10@bandit:~$ base64 --decode data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```