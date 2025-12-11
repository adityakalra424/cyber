given a zip file, unziped it and got `ukn_reality.jpg` and then ran file but nothing came and ran exiftool and got a base64 encoded string `cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==` decoded it and 
got the flag 
```
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
akalra@fedora:~/Desktop/picoctf/forencis$ ls
ukn_reality.jpg  unknown.zip
akalra@fedora:~/Desktop/picoctf/forencis$ file ukn_reality.jpg
ukn_reality.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 4308x2875, components 3
akalra@fedora:~/Desktop/picoctf/forencis$ exiftool ukn_reality.jpg
ExifTool Version Number         : 13.10
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:12 05:35:55+05:30
File Access Date/Time           : 2025:12:11 13:02:40+05:30
File Inode Change Date/Time     : 2025:12:11 13:02:40+05:30
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
akalra@fedora:~/Desktop/picoctf/forencis$ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==" | base64 -d
picoCTF{ME74D47A_HIDD3N_6a9f5ac4}
```
**FLAG - picoCTF{ME74D47A_HIDD3N_6a9f5ac4}**
