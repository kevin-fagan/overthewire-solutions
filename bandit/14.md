# Level 14

### Instructions
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

### Solutions
1. Ensure you are logged in as `bandit13`:
```
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

1. We can only access `/etc/bandit_pass/bandit14` if we are logged in as `bandit14`. We can ssh into `localhost` as `bandit14` using the private key provided to us:

```shell
bandit13@bandit:~$ ssh bandit14@localhost -p 2220 -i sshkey.private
```

3. Once we are logged in as `bandit14`, we can read the password from desired file:
```shell
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```