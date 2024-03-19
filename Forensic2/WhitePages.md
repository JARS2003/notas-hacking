## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/forensic/WhitePages]
└─$ python exp.py

        picoCTF

        SEE PUBLIC RECORDS & BACKGROUND REPORT
        5000 Forbes Ave, Pittsburgh, PA 15213
        picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}
        
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/WhitePages]
└─$ 

┌──(jars㉿jars)-[~/picoCTF/forensic/WhitePages]
└─$ cat exp.py        
from pwn import *

with open('whitepages.txt', 'rb') as f:
    data = f.read()  
data = data.replace(b'\xe2\x80\x83', b'0').replace(b' ', b'1')


data = data.decode("ascii")


print(unbits(data).decode("ascii"))
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/WhitePages]
└─$ 

```
## Notas adicionales
## Referencias 