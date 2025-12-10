# THE ROOT
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
```
# PROGRAM AND ABSOLUTE PATHS
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
```
# POSITION THY SELF
```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/bin
hacker@paths~position-thy-self:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
```
# POSTION ELSEWHERE 
```
hacker@paths~position-elsewhere:/etc$ /challenge/run
Starting level 1.
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Moving on to level 2
Please use the `cd` utility to change directory to /var/lib/apt/lists
hacker@paths~position-elsewhere:/etc$ cd /var/lib/apt/lists
hacker@paths~position-elsewhere:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Moving on to level 3
Please use the `cd` utility to change directory to /etc/apt/sources.list.d
hacker@paths~position-elsewhere:/var/lib/apt/lists$ cd /etc/apt/sources.list.d
hacker@paths~position-elsewhere:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Moving on to level 4
Please use the `cd` utility to change directory to /usr/share/doc/fontconfig
hacker@paths~position-elsewhere:/etc/apt/sources.list.d$ cd /usr/chare/doc/fontconfig
bash: cd: /usr/chare/doc/fontconfig: No such file or directory
hacker@paths~position-elsewhere:/etc/apt/sources.list.d$ cd /usr/share/doc/fontconfig
hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Moving on to level 5
Please use the `cd` utility to change directory to /usr/share/zoneinfo/posix/Asia
hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$ cd /usr/share/zoneinfo/posix/Asia
hacker@paths~position-elsewhere:/usr/share/zoneinfo/posix/Asia$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
```
# IMPLICIT RELATIVE PATHS , FROM /
```
hacker@paths~implicit-relative-paths-from-:~$ challenge/run
bash: challenge/run: No such file or directory
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
```
# EXPLICIT RELATIVE PATHS , FROM /
```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge/run/.
bash: challenge/run/.: Not a directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
```
# IMPLICIT RELATIVE PATHS
```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
```
# HOME SWEET HOME 
```
hacker@paths~home-sweet-home:~$ /challenge/run ~/.
Writing the file to /home/hacker/.!
/challenge/run: line 29: /home/hacker/.: Is a directory
... and reading it back to you:
cat: /home/hacker/.: Is a directory
hacker@paths~home-sweet-home:~$ /challennge/run ~/
bash: /challennge/run: No such file or directory
hacker@paths~home-sweet-home:~$ /challenge/run ~/
Writing the file to /home/hacker/!
/challenge/run: line 29: /home/hacker/: Is a directory
... and reading it back to you:
cat: /home/hacker/: Is a directory
hacker@paths~home-sweet-home:~$ /challenge/run ~
Writing the file to /home/hacker!
/challenge/run: line 29: /home/hacker: Is a directory
... and reading it back to you:
cat: /home/hacker: Is a directory
hacker@paths~home-sweet-home:~$ cd 
hacker@paths~home-sweet-home:~$ ls
flag  not-the-flag
hacker@paths~home-sweet-home:~$ /challenge/run ~/flag
The argument you provided must not have been longer than 3 characters (it's 
currently 6 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
```
