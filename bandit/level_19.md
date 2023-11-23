# Level 19

### Instructions
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

### Solutions
1. Logging into this challenge is a bit different. If you login as `bandit18` as we previosuly had, you will notice that you your connection is terminated upon login. We can use the `-T` flag to get around this. The `-T` flag `Disabled pseudo-terminal allocation`. Typically, when you connect to a remote server using SSH, a pseudo-terminal (or pseudoterminal, pty) is allocated for that session. This pty allows interactive shell sessions and supports features like command-line editing, command history, and job control. However, in some cases, you might not want to allocate a pty. When you use the `-T` option with the `ssh` command, it disables the allocation of a pseudo-terminal
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 -T
```

1. Upon login, you wont be prompted with any messages but you will still be able to interact with host:
```shell
ls
readme
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```