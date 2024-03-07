
## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)
## Solución
```
jars-picoctf@webshell:~$ curl -I HEAD -i http://mercury.picoctf.net:45028/         
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8

jars-picoctf@webshell:~$ 
```
```

```
## Notas adicionales
## Referencias 
