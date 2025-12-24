Opened the website and right clicked and inspected the website nothing in the code, then i tried to login and it showed this, So i went to the cookies 
<img width="1917" height="1069" alt="image" src="https://github.com/user-attachments/assets/ddae80cc-82b9-49f4-9a53-8dacde9eb6db" />
the cookie was url encoded so clicked the little option to decode it and got a base64 string, decoded it and got the flag 
```
cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E2RkEwN0Q4fQ==
```
```
akalra@akalra:~$ echo "cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E2RkEwN0Q4fQ==" | base64 -d
picoCTF{c00k1e_m0nster_l0ves_c00kies_A6FA07D8}
```
**FLAG - picoCTF{c00k1e_m0nster_l0ves_c00kies_A6FA07D8}**
