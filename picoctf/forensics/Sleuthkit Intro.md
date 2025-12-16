did what the challenge asked and got the size as 202752 and then connected to nc and got the flag 
```
akalra@akalra:/tmp$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
akalra@akalra:/tmp$ nc saturn.picoctf.net 60646
What is the size of the Linux partition in the given disk image?
Length in sectors: 512
512
That is not correct. Feel free to try again.
^Z  
[3]+  Stopped                 nc saturn.picoctf.net 60646
akalra@akalra:/tmp$ nc saturn.picoctf.net 60646
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```
**FLAG = picoCTF{mm15_f7w!}**
