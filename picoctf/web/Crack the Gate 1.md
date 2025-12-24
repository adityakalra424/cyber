I checked the hints given in the challenge, it said `Developers sometimes leave notes in the code` so i opened the site, right clicked and inspected and i got `<!-- ABGR: Wnpx - grzcbenel olcnff: hfr urnqre "K-Qri-Npprff: lrf" -->`
the second hint said it was rot13 encoding so i went to `dcode` and decoded the text `<!-- NOTE: Jack - temporary bypass: use header "X-Dev-Access: yes" -->` so ig i have to put `X-Dev-Access: yes` header
in the request when i login, so i opened burp suite and did it and got the flag 

<img width="1917" height="1069" alt="Screenshot from 2025-12-24 15-07-38" src="https://github.com/user-attachments/assets/1403e26a-1b3b-43cd-b609-6c4e4a496616" />
**FLAG - picoCTF{brut4_f0rc4_1a386e6f}**
