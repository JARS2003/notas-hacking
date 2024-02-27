## Objetivo
## Datos de acceso al nivel
bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Solución
```
:shell
bandit26@bandit:~$ id
uid=11026(bandit26) gid=11026(bandit26) groups=11026(bandit26)
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ cat text.txt
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do id cat /etc/bandit_pass/bandit27
id: ‘cat’: no such user
id: ‘/etc/bandit_pass/bandit27’: no such user
bandit26@bandit:~$ ls -l bandit27-do
-rwsr-x--- 1 bandit27 bandit26 14876 Oct  5 06:19 bandit27-do
bandit26@bandit:~$ ls -l bandit27-do cat /etc/bandit_pass/bandit27
ls: cannot access 'cat': No such file or directory
-rwsr-x--- 1 bandit27 bandit26 14876 Oct  5 06:19 bandit27-do
-r-------- 1 bandit27 bandit27    33 Oct  5 06:19 /etc/bandit_pass/bandit27
bandit26@bandit:~$ ./bandit27-do id cat /etc/bandit_pass/bandit27
id: ‘cat’: no such user
id: ‘/etc/bandit_pass/bandit27’: no such user
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```
## Notas adicionales
Es igual que el pasado solo que aquí se ejecuto el archivo junto con el cat para obtener la contraseña.
## Referencias 
