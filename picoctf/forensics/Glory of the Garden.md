The challenge gave a file, hint said hexeditor but i didnt want to open a hexeditor to find the flag so i ran strings 
```
strings garden.jpg | grep "picoCTF"
```
and i got the flag 
```
akalra@fedora:~/Desktop/picoctf/forencis$ strings garden.jpg | grep "picoCTF"
Here is a flag: picoCTF{more_than_m33ts_the_3y333f84d7c}
akalra@fedora:~/Desktop/picoctf/forencis$ 

```
**FLAG - picoCTF{more_than_m33ts_the_3y333f84d7c}**
