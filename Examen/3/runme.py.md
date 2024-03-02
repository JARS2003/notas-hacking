## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución
```
┌──(jars㉿kali)-[/tmp/jars]
└─$ wget https://artifacts.picoctf.net/c/34/runme.py                                                         
--2024-03-01 19:22:37--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.225.60, 3.161.225.11, 3.161.225.62, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.225.60|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py                                                   100%[=======================================================================================================================================>]     270  --.-KB/s    in 0s      

2024-03-01 19:22:38 (177 MB/s) - ‘runme.py’ saved [270/270]

                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ ls
runme.py
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python runme.py 
picoCTF{run_s4n1ty_run}
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ 


```
## Notas adicionales
## Referencias 