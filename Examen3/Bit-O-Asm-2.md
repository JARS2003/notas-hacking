## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/asm2]
└─$ ls
disassembler-dump0_b.txt
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm2]
└─$ cat disassembler-dump0_b.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm2]
└─$ python3 -c "print(int('0x9fe1a', 16))"

654874
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm2]
└─$ 

picoCTF{653114}

```
## Notas adicionales
## Referencias 