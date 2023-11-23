# Level 13

### Instructions
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

### Solutions
1. Ensure you are logged in as `bandit12`:
```
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

2. We need to decompress the file appropriately. This may take some playing around with as the file was compressed using different commands, multiple times. The first step is to make a copy of the original file and move it into the `tmp` directory:
```shell
bandit12@bandit:/tmp/kevin$ mv data.txt /tmp/kevin
bandit12@bandit:/tmp/kevin$ cp data.txt /tmp/kevin
```

3. `data.txt` contains the hex dump of the file. We can reverse the hex dump by using the `xxd` command: 
```shell
bandit12@bandit:/tmp/kevin$ xxd -r data.txt > hex_revert
```

4. The last step is to decompress the file multiple times. I highly recommend reading the `man` pages for each command:
```shell
bandit12@bandit:/tmp/kevin$ gzip -d -c hex_revert | bunzip > unzip
bandit12@bandit:/tmp/kevin$ tar -xf unzip
bandit12@bandit:/tmp/kevin$ tar -xf data5.bin
bandit12@bandit:/tmp/kevin$ bzip2 -d data6.bin
bandit12@bandit:/tmp/kevin$ tar -xf data6.bin.out
bandit12@bandit:/tmp/kevin$ gzip -d -c data8.bin
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
