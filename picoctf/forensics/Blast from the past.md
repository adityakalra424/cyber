Changed the time using the exiftool tool 
```
xiftool -SubSecModifyDate="1970:01:01 00:00:00.001" original.jpg
```
then i ran the checker and corrected the time accordingly which the command
```
exiftool -(the catogory)="1970:01:01 00:00:00.001" original.jpg
```
but couldnt change the timestamp and then i tried using touch command but i couldnt do it, then found the website 
```
https://stackoverflow.com/questions/78185037/how-to-edit-the-samsung-trailer-tag-timestamp
```
samsung timestamp are binary and i could change it in the hexeditor only the 13 bytes, now the unix timestamp of `1970:01:01 00:00:00.001` was 0000000000001 so i changed it and got the flag 
i searched for the 13 bytes where to change them and the changed them 

<img width="700" height="186" alt="Screenshot_20251211_183832" src="https://github.com/user-attachments/assets/d5ecd05b-3c19-4201-8ec1-b0a563630197" />

```
akalra@fedora:~/Desktop/picoctf/forencis$ nc -w 2 mimas.picoctf.net 54378 < original.jpg
akalra@fedora:~/Desktop/picoctf/forencis$ nc mimas.picoctf.net 52209
MD5 of your picture:
372824913372cbf2c7250a3a5c15fb74  test.out

Checking tag 1/7
Looking at IFD0: ModifyDate
Looking for '1970:01:01 00:00:00'
Found: 1970:01:01 00:00:00
Great job, you got that one!

Checking tag 2/7
Looking at ExifIFD: DateTimeOriginal
Looking for '1970:01:01 00:00:00'
Found: 1970:01:01 00:00:00
Great job, you got that one!

Checking tag 3/7
Looking at ExifIFD: CreateDate
Looking for '1970:01:01 00:00:00'
Found: 1970:01:01 00:00:00
Great job, you got that one!

Checking tag 4/7
Looking at Composite: SubSecCreateDate
Looking for '1970:01:01 00:00:00.001'
Found: 1970:01:01 00:00:00.001
Great job, you got that one!

Checking tag 5/7
Looking at Composite: SubSecDateTimeOriginal
Looking for '1970:01:01 00:00:00.001'
Found: 1970:01:01 00:00:00.001
Great job, you got that one!

Checking tag 6/7
Looking at Composite: SubSecModifyDate
Looking for '1970:01:01 00:00:00.001'
Found: 1970:01:01 00:00:00.001
Great job, you got that one!

Checking tag 7/7
Timezones do not have to match, as long as it's the equivalent time.
Looking at Samsung: TimeStamp
Looking for '1970:01:01 00:00:00.001+00:00'
Found: 1970:01:01 00:00:00.001+00:00
Great job, you got that one!

You did it!
picoCTF{71m3_7r4v311ng_p1c7ur3_83ecb41c}
```
**FLAG -picoCTF{71m3_7r4v311ng_p1c7ur3_83ecb41c} **
