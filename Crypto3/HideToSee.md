## Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/239/atbash.jpg).
## Solución
```
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$  sudo apt install steghide 

[sudo] password for jars: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
steghide is already the newest version (0.5.1-15).
0 upgraded, 0 newly installed, 0 to remove and 1522 not upgraded.
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$ steghide extract -sf atbash.jpg 

Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$ steghide extract -sf atbash.jpg

Enter passphrase: 
the file "encrypted.txt" does already exist. overwrite ? (y/n) n
steghide: did not write to file "encrypted.txt".
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$ ls
atbash.jpg  encrypted.txt
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$ cat encrypted.txt          
krxlXGU{zgyzhs_xizxp_1u84w779}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/cripto/toSee]
└─$ 
picoCTF{atbash_crack_1f84d779}

```
## Notas adicionales
## Referencias 