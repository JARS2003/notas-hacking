## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/asm3]
└─$ cat disassembler-dump0_c.txt          
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4
<+29>:    mov    eax,DWORD PTR [rbp-0xc]
<+32>:    imul   eax,DWORD PTR [rbp-0x8]
<+36>:    add    eax,0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]
<+47>:    pop    rbp
<+48>:    ret
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm3]
└─$ python                                
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> resultado_multiplicacion = 0x9fe1a * 0x4
>>> 
>>> resultado_suma = resultado_multiplicacion + 0x1f5
>>> 
>>> resultado_decimal = int(resultado_suma)
>>> 
>>> print(resultado_decimal)
2619997
>>> 



picoCTF{2619997}
```
## Notas adicionales
## Referencias 