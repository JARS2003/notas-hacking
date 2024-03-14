## Objetivo
How well can you perfom basic binary operations?
Start searching for the flag here nc titan.picoctf.net 49152

- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Solución


```
┌──(aratt㉿kali)-[/tmp/tmp.WLxRuf2KIL]
└─$ nc titan.picoctf.net 49152

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00100100
Binary Number 2: 11010100


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 1001000
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11110100
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 1101010
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1110111010000
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111000
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000100
Correct!

Enter the results of the last operation in hexadecimal: 4

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
                                                                                                                                                                                                                                            
┌──(aratt㉿kali)-[/tmp/tmp.WLxRuf2KIL]
└─$ 

```
## Notas adicionales

## Referencias 