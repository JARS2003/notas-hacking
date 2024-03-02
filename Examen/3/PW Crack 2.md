## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Solución
```
┌──(jars㉿kali)-[/tmp/jars]
└─$ nano level2.py 
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python3                       
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) 
'39ce'
>>> 
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ 

```
## Notas adicionales
## Referencias 