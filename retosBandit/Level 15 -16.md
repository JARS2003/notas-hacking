
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
```
    Start Time: 1708457303
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$ history
    1  clear
    2  nc localhost 30001
    3  openssl s_client -connect localhst 30001
    4  openssl s_client -connect localhost:30001
    5  history
bandit15@bandit:~$
```
## Notas adicionales

## Referencias 
https://www.feistyduck.com/library/openssl-cookbook/online/