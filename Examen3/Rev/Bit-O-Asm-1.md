## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/asm1]
└─$ ls
disassembler-dump0_a.txt
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm1]
└─$ cat disassembler-dump0_a.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm1]
└─$ python3 -c "print(int('0x30', 16))"

48
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/asm1]
└─$ 

picoCTF{48}
```
## Notas adicionales
## Referencias 