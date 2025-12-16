learnt slueth kit and used some commands and some video and i did strings but there were too many flags, then i used the hint and it said to isolate the partition and then i searched it and 
used the mmcat command and then i did the strings command to search it but i did try to find a flag file but i couldnt so i just did strings 
```
akalra@akalra:~/Desktop/picoctf/forencis$ mmls disko-2.dd
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000053247   0000051200   Linux (0x83)
003:  000:001   0000053248   0000118783   0000065536   Win95 FAT32 (0x0b)
004:  -------   0000118784   0000204799   0000086016   Unallocated
akalra@akalra:~/Desktop/picoctf/forencis$ mmcat disko-2.dd 2 > linux.dd
akalra@akalra:~/Desktop/picoctf/forencis$ ls
disk.img.gz  disko-2.dd  dump.pcap  Flag.pdf  flag.zip  linux.dd
akalra@akalra:~/Desktop/picoctf/forencis$ strings linux.dd | grep "pico"
picoCTF{4_P4Rt_1t_i5_90a3f3d1}
piconv
:/icons/appicon
piconv
piconv
piconv
# $Id: piconv,v 2.8 2016/08/04 03:15:58 dankogai Exp $
piconv -- iconv(1), reinvented in perl
  piconv [-f from_encoding] [-t to_encoding]
  piconv -l
  piconv -r encoding_alias
  piconv -h
B<piconv> is perl version of B<iconv>, a character encoding converter
a technology demonstrator for Perl 5.8.0, but you can use piconv in the
piconv converts the character encoding of either STDIN or files
Therefore, when both -f and -t are omitted, B<piconv> just acts
akalra@akalra:~/Desktop/picoctf/forencis$
```
and i got the flag 
**FLAG = picoCTF{4_P4Rt_1t_i5_90a3f3d1}**


```
