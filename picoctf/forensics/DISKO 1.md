The file given was a gz file, used gzip to extract it and ran strings to get the file 

**command to decompress the file**
```
akalra@fedora:~/Desktop/picoctf/forencis$ gzip -d disko-1.dd.gz
```

```
akalra@fedora:~/Desktop/picoctf/forencis$ strings disko-1.dd | grep -i "picoctf"
picoCTF{1t5_ju5t_4_5tr1n9_c63b02ef}
```

what is a DOS FILE ?
```
akalra@fedora:~/Desktop/picoctf/forencis$ file disko-1.dd
disko-1.dd: DOS/MBR boot sector, code offset 0x58+2, OEM-ID "mkfs.fat", Media descriptor 0xf8, sectors/track 32, heads 8, sectors 102400 (volumes > 32 MB), FAT (32 bit), sectors/FAT 788, serial number 0x241a4420, unlabeled
akalra@fedora:~/Desktop/picoctf/forencis$ 
```
