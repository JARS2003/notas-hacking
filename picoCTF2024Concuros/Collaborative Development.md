## Objetivo
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)
## Solución

Primero se descomprime el archivo,despues este es un repositorio,y en este intercambiamos entre ramas y le hacemos cat a los archivos flag.py


```
ulises1612-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
ulises1612-picoctf@webshell:~$ cd drop-in/
ulises1612-picoctf@webshell:~/drop-in$ ls
flag.py
ulises1612-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
ulises1612-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
ulises1612-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')ulises1612-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
ulises1612-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')ulises1612-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
ulises1612-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("w0rk_e4b79efb}")
ulises1612-picoctf@webshell:~/drop-in$ 

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}

```
## Notas adicionales

## Referencias 