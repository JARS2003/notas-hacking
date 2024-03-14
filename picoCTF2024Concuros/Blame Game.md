## Objetivo
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Solución

se descomprime el archivo y despues en el repositorio se le hace un git log,este da muchos resultados por lo que se le aplica un grep para ver si se encuentra la bandera.


```
SyntaxError: '(' was never closed
ulises1612-picoctf@webshell:~/drop-in$ cat message.py 
print("Hello, World!"
ulises1612-picoctf@webshell:~/drop-in$ git branch
ulises1612-picoctf@webshell:~/drop-in$ git log 
ulises1612-picoctf@webshell:~/drop-in$ git log | grep pico

Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF{@sk_th3_1nt3rn_b64c4705} <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
ulises1612-picoctf@webshell:~/drop-in$ ^C

```
## Notas adicionales

## Referencias 