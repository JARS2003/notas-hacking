## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso al nivel
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solución
```
bandit8@bandit:~$ wc -l data.txt
1001 data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```
## Notas adicionales
sort ordena las lineas de texto , 
uniq las filtra, el -u muestra las lineas unicas, -c muestra las veces que se repite
## Referencias 