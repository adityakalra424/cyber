# CAT
```
cat flag
```
# CATTING ABSOLUTE PATHS
```
cat /flag

```
# MORE CATTING PRACTISE 
```
hacker@commands~more-catting-practice:~$ cat /usr/share/apache2/flag
```
# GREPPING
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ cat /challenge/data.txt | grep "pwn.college"
```
# COMPARING FILES
```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
20a21
```
# LISTING FILES
```
hacker@commands~listing-files:~$ ls /challenge
15750-renamed-run-26090  DESCRIPTION.md
hacker@commands~listing-files:~$ cat /challenge/15750-renamed-run-26090 
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:~$ /challenge/15750-renamed-run-26090 
Yahaha, you found me! Here is your flag:

```
# TOUCHING FILES
```
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:


```
# REMOVING FILES
```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/run
bash: /challenge/run: No such file or directory
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
```
# MOVING FILES
```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
```
# COPYING FILES
```
hacker@commands~copying-files:~$ cp /flag /tmp/hack-the-planet
Correct! Performing 'cp /flag /tmp/hack-the-planet'.
hacker@commands~copying-files:~$ /challenge/check
Congrats! You successfully copied the flag to /tmp/hack-the-planet! Here it is:
```
# HIDDEN FILES
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.  ..  .dockerenv  .flag-182752846624512  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:/$ cat .flag-182752846624512

```
# AN EPIC FILESYSTEM QUEST 
```
DO IT YOURSELF 
```
# MAKING DIRECTORIES
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:

```
# FINDING FILES
```

```
# LINKNING FILES
