## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
```
┌──(jars㉿kali)-[/tmp/jars]
└─$ ls
level1.flag.txt.enc  level1.py
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ nano level1.py 
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}

```
## Notas adicionales
## Referencias 