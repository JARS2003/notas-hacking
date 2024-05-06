## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/Transformation]
└─$ ls
enc
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/Transformation]
└─$ cat enc 
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸強㕤㐸㤸扽                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/Transformation]
└─$ nano enc   
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/Transformation]
└─$ python       
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> encoded_flag = open("enc").read()
>>> flag = ""
>>> for i in range(0, len(encoded_flag)):
...     character1 = chr((ord(encoded_flag[i]) >> 8))
...     character2 = chr(encoded_flag[i].encode('utf-16be')[-1])
...     flag += character1
...     flag += character2
... 
>>> print("Flag: " + flag)
Flag: picoCTF{16_bits_inst34d_of_8_75d4898b}
>>> 

```
## Notas adicionales
## Referencias 