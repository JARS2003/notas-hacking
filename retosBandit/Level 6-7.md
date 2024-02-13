## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel
bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
## Solución
```
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```
## Notas adicionales
 2>/dev/null manda los errores a otro lado, dejando solo las correctas
## Referencias 
