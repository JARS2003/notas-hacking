## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de acceso al nivel
bandit21
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
## Solución
```
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
bandit21@bandit:~$ history
    1  clear
    2  ls
    3  cat
    4  clear
    5  cat /etc/crontab
    6  ls /etc/cron.d
    7  ls -la /etc/cron.d
    8  cat /etc/cron.d/cronjob_bandit22
    9  cat /usr/bin/cronjob_bandit22.sh
   10  clear
   11  cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
   12  history
bandit21@bandit:~$

```
## Notas adicionales
## Referencias 
