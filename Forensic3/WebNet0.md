## Objetivo

## Solución
```
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet0]
└─$ wireshark capture.pcap  
                                                                                                                  
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet0]
└─$ wireshark capture.pcap &
[1] 2873
                                                                                                                  
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet0]
└─$ 
Ponemos la llave para que asi se desencripte el trafico y despues buscar en los detalles la palabra picoCTF
"Pico-Flag: picoCTF{nongshim.shrimp.crackers}\x0d\x0a"
```
## Notas adicionales
## Referencias 