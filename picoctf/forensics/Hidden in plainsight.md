The challenge gave a png file, checked the metadata and found a comment " c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9 " , decoded it (base 64) and got "steghide:cEF6endvcmQ= " , decoded "cEF6endvcmQ= " which was "pAzzword", this meant i had to use steghide and extract
the flag using the passphare "pAzzword" which i did and i got the flag 

**METADATA**
```
kalra@fedora:~/Desktop/picoctf/forencis$ exiftool img.jpg
ExifTool Version Number         : 13.10
File Name                       : img.jpg
Directory                       : .
File Size                       : 73 kB
File Modification Date/Time     : 2025:12:10 23:19:12+05:30
File Access Date/Time           : 2025:12:10 23:19:31+05:30
File Inode Change Date/Time     : 2025:12:10 23:19:17+05:30
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Comment                         : c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9
Image Width                     : 640
Image Height                    : 640
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 640x640
Megapixels                      : 0.410
```
**STEGHIDE COMMAND**
```
akalra@fedora:~/Desktop/picoctf/forencis$ steghide extract -sf img.jpg -p pAzzword
wrote extracted data to "flag.txt".
```
```
akalra@fedora:~/Desktop/picoctf/forencis$ ls
confidential.pdf  flag.txt  img.jpg
akalra@fedora:~/Desktop/picoctf/forencis$ cat flag.txt
picoCTF{h1dd3n_1n_1m4g3_67479645}
```
**FLAG - picoCTF{h1dd3n_1n_1m4g3_67479645}**
