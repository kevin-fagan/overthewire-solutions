# Level 12

### Instructions
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

### Solutions
1. Ensure you are logged in as `bandit11`:
```
ssh bandit11@bandit.labs.overthewire.org -p 2220
```
1. When it comes to encoding, decoding, enryption or dectyption of text, I prefer to use cyberchef.org. I find it easier and faster than attempting to use a command like `tr` to perform tranlastion on a string:
```text
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi = The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```