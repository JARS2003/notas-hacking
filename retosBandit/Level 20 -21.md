
## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución
```
bandit20@bandit:~$ nc -lnvp 2003 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 137634
bandit20@bandit:~$ Listening on 0.0.0.0 2003
./suconnect 2003
Connection received on 127.0.0.1 46252
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ jobs
[1]+  Done                    nc -lnvp 2003 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$
```
## Notas adicionales
## Referencias 
