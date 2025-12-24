I look at the website and cant see anything different so i try to login and i see a secure.js file appear and that file was checking the username and the password
<img width="1917" height="1069" alt="image" src="https://github.com/user-attachments/assets/52f04d30-2a5a-420a-b4c3-1d789a2912b0" />

```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
then i login to the website using the username and password and got the flag 
<img width="1917" height="1069" alt="image" src="https://github.com/user-attachments/assets/cdf258ac-5fd4-4872-9792-97e0cb55207a" />


**FLAG - picoCTF{j5_15_7r4n5p4r3n7_05df90c8}**
