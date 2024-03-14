## Objetivo
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/1/enc_flag).
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ wget https://artifacts.picoctf.net/c_titan/1/enc_flag      
--2024-03-14 12:58:35--  https://artifacts.picoctf.net/c_titan/1/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.103, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                                                   100%[=======================================================================================================================================>]      73  --.-KB/s    in 0s      

2024-03-14 12:58:35 (88.8 MB/s) - ‘enc_flag’ saved [73/73]

                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ ls
enc_flag
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ cat enc_flag   
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ nano decodificador
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ ls
enc_flag
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ nano decodificador.py
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ python decodificador.py 
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='

                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ nano decodificador.py 
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ python decodificador.py
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ 
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ nano decodificador.py  
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ python decodificador.py
Traceback (most recent call last):
  File "/home/jars/picoCTF/retosEquipo/interencdec/decodificador.py", line 4, in <module>
    decoded_text = base64.b64decode(encoded_text).decode('utf-8')
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/base64.py", line 88, in b64decode
    return binascii.a2b_base64(s, strict_mode=validate)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
binascii.Error: Incorrect padding
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ nano decodificador.py  
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$ python decodificador.py
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/interencdec]
└─$   
picoCTF{caesar_d3cr9pt3d_ea60e00b}
Se rota 19 veces
```
## Notas adicionales
## Referencias 