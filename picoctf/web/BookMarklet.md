I opened the website
<img width="1917" height="1069" alt="image" src="https://github.com/user-attachments/assets/0b92d5b3-4b19-485b-a3c1-b69de28b5c87" />
This is what i got 
```
javascript:(function() { var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÉÕËÆÒÇÚËí"; var key = "picoctf"; var decryptedFlag = ""; for (var i = 0; i < encryptedFlag.length; i++)
 { decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256); } alert(decryptedFlag); })();
```
wrote a script and got the flag
```
encrypted_flag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÉÕËÆÒÇÚËí"
key = "picoctf"

decrypted_flag = ""

for i in range(len(encrypted_flag)):
    decrypted_char = chr(
        (ord(encrypted_flag[i]) - ord(key[i % len(key)]) + 256) % 256
    )
    decrypted_flag += decrypted_char

print(decrypted_flag)
```
**FLAG - picoCTF{p@g3_turn3r_cebccdfe}**
