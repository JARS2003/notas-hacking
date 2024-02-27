## Objetivo

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Solución
```
jars-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
--2024-02-27 18:35:41--  https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                          100%[===============================================>]  10.68K  --.-KB/s    in 0s      

2024-02-27 18:35:41 (327 MB/s) - 'warm' saved [10936/10936]

jars-picoctf@webshell:~$ chmod +x warm 
jars-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
jars-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```
## Notas adicionales
## Referencias 