The challenge mentioned metadata so ran the command exiftool and got the flag 
```
kalra@fedora:~/Desktop/picoctf/forencis$ file confidential.pdf
confidential.pdf: PDF document, version 1.7, 1 page(s)
akalra@fedora:~/Desktop/picoctf/forencis$ cat confidential.pdf | grep -i "ctf"
akalra@fedora:~/Desktop/picoctf/forencis$ exiftool confidential.pdf
ExifTool Version Number         : 13.10
File Name                       : confidential.pdf
Directory                       : .
File Size                       : 183 kB
File Modification Date/Time     : 2025:12:10 23:09:10+05:30
File Access Date/Time           : 2025:12:10 23:11:04+05:30
File Inode Change Date/Time     : 2025:12:10 23:11:04+05:30
File Permissions                : -rw-r--r--
File Type                       : PDF
File Type Extension             : pdf
MIME Type                       : application/pdf
PDF Version                     : 1.7
Linearized                      : No
Page Count                      : 1
Producer                        : PyPDF2
Author                          : cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8zNTc4NzM5YX0=
akalra@fedora:~/Desktop/picoctf/forencis$ echo "cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8zNTc4NzM5YX0=" | base64 -d
picoCTF{puzzl3d_m3tadata_f0und!_3578739a}
```
**FLAG -  picoCTF{puzzl3d_m3tadata_f0und!_3578739a} **
