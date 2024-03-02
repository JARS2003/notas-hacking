## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 52682`
## Solución
```
──(jars㉿kali)-[/tmp/jars]
└─$ nc saturn.picoctf.net 52682
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python3         
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
'picoCTF{gl17ch_m3_n07_bda68f75}'
>>> 
KeyboardInterrupt

```
## Notas adicionales
## Referencias 