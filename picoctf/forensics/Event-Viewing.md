The challenge gave a evtx file so installed `libevtx` and got these tools `evtxinfo evtxdump evtxexport` .
Used evtxexport to get a evtx file into a more readable format such as a xml file 
```
evtxexport Windows_Logs.evtx > output.xml
```
i opened the output.xml and went to view source and started going through it and found msiinstaller installing `Totally_Legit_Software` there i got the first part of the flag `cGljb0NURntFdjNudF92aTN3djNyXw==`
then i searched for `Totally_Legit_Software` and found an event where it was running the exe file and got the second part of the flag `MXNfYV9wcjN0dHlfdXMzZnVsXw==`
then i searched `shutdown` beacuse `Totally_Legit_Software` was running `shutdown.exe` as well and then i got the third part of the flag `dDAwbF84MWJhM2ZlOX0=`
then decoded the base64 encoded strings and got the flag 
```
akalra@fedora:~/Desktop/picoctf/forencis$ ls
disko-2.dd  output.json  output.xml  Windows_Logs.evtx
akalra@fedora:~/Desktop/picoctf/forencis$ echo "cGljb0NURntFdjNudF92aTN3djNyXw==" | base64 -d
picoCTF{Ev3nt_vi3wv3r_akalra@fedora:~/Deskecho "MXNfYV9wcjN0dHlfdXMzZnVsXw==" | base64 -d
1s_a_pr3tty_us3ful_akalra@fedora:~/Desktopecho "dDAwbF84MWJhM2ZlOX0=" | base64 -d
t00l_81ba3fe9}akalra@fedora:~/Desktop/picoctf/forencis$
```
**FLAG - picoCTF{Ev3nt_vi3wv3r_1s_a_pr3tty_us3ful_t00l_81ba3fe9}**
