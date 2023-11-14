# Level 5

### Instructions
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

### Solutions
1. Ensure you are logged in as `bandit4`:
   <br>
    ```
    ssh bandit4@bandit.labs.overthewire.org -p 2220
    ```

2. There are 10 within the `inhere` directory. One of these files contains the password for the next level. We can cat each file one by one, or we can cat them all at once like such:
   <br>
    ```shell
    bandit4@bandit:~/inhere$ cat ./-file*
    QRrtZ�i�	�H
                    |��ȧ����^��7L3��Y�ͯ	Ŵ����E�Y�ܚ	�V&��h�F���y���O̫��`�\�-⃐�Hx��2��K��i�x�#e�>��VO��p{�	���MUb4����gQ��eE}:�g���j8������<.�e��S��e 0�����]7�������b�<�~G=1��������B׃�"
                                                ���W��9ؽ5lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
    ���K�~�+��9"T���*Z$���"�r�
    �Z�\�������ж�q���7����/�n��n
    ```
    
    The password for the next level is the only text within the above snippet that is human readable: `lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR`
