## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.
## Solución
```

┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ cat rev_this 
picoCTF{w1{1wq8/7376j.:}                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ file rev                              
rev: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=523d51973c11197605c76f84d4afb0fe9e59338c, not stripped
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ file rev_this 
rev_this: ASCII text, with no line terminators
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ open exp.py 
import os

import mmap

  

def memory_map(filename, access=mmap.ACCESS_READ):

size = os.path.getsize(filename)

fd = os.open(filename, os.O_RDONLY)

return mmap.mmap(fd, size, access=access)

  

with memory_map("rev_this") as bin_file:

for i in range(8):

print(chr(bin_file[i]), end = '')

for i in range(8, 23):

if (i & 1) == 0:

print(chr(bin_file[i] - 5), end = '')

else:

print(chr(bin_file[i] + 2), end = '')

print (chr(bin_file[23]))                                                                                                                                                          
┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ python exp.py 
picoCTF{r3v3rs312528e05}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/reversing/rev]
└─$ 


```
## Notas adicionales
## Referencias 