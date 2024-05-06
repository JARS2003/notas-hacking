## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/asm4]
└─$ cat disassembler-dump0_d.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    cmp    DWORD PTR [rbp-0x4],0x2710
<+29>:    jle    0x55555555514e <main+37>
<+31>:    sub    DWORD PTR [rbp-0x4],0x65
<+35>:    jmp    0x555555555152 <main+41>
<+37>:    add    DWORD PTR [rbp-0x4],0x65
<+41>:    mov    eax,DWORD PTR [rbp-0x4]
<+44>:    pop    rbp
<+45>:    ret
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm4]
└─$ python 
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> valor_hexadecimal = 0x9fe1a
>>> 
>>> valor_comparacion = 0x2710
>>> 
>>> if valor_hexadecimal <= valor_comparacion:
...     resultado = valor_hexadecimal + 0x65
... else:
...     resultado = valor_hexadecimal - 0x65
... 
>>> print(resultado)
654773

picoCTF{654773}
```
## Notas adicionales
## Referencias 