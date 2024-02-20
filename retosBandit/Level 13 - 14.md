## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
## Datos de acceso al nivel
bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
## Solución
```

bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ history
    1  cat /etc/bandit_pass/bandit14
    2  history
bandit14@bandit:~$ exit
logout
Connection to localhost closed.
bandit13@bandit:~$ history
    1  clear
    2  ls
    3  ls -la
    4  cat /etc/bandit_pass/bandit13
    5  cat /etc/bandit_pass/bandit14
    6  cat sshkey.private
    7  ssh -i sshkey.private bandit14@localhost -p2220
    8  history
bandit13@bandit:~$
```
## Notas adicionales
Se puede acceder a otro bandit con el .private
## Referencias 
