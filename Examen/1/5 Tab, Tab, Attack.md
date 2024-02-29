## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip)

## Solución
```
┌──(jars㉿kali)-[~]
└─$ wgets https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
Command 'wgets' not found, did you mean:
  command 'wget' from deb wget
  command 'wget2' from deb wget2
Try: sudo apt install <deb name>
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~]
└─$ wget  https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
--2024-02-27 14:37:12--  https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: ‘Addadshashanammu.zip’

Addadshashanammu.zip                                       100%[========================================================================================================================================>]   4.41K  --.-KB/s    in 0s      

2024-02-27 14:37:13 (48.0 MB/s) - ‘Addadshashanammu.zip’ saved [4520/4520]

                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~]
└─$ ls
Addadshashanammu.zip  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~]
└─$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~]
└─$ ls
Addadshashanammu  Addadshashanammu.zip  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~]
└─$ cd Addadshashanammu 
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/Addadshashanammu]
└─$ ls
Almurbalarammi
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/Addadshashanammu]
└─$ cat Almurbalarammi 
cat: Almurbalarammi: Is a directory
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/Addadshashanammu]
8#TT 1tt$D���o�Nrammi  
�� ��0)@▒       (;▒�                                                                                                                                                                                                                                            ddadshashanammu/Almurbalarammi]
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls
fang-of-haynekhtnamet
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ pwd                                                                      
/home/jars/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ cd /                                                                     
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[/]
8#TT 1tt$D���o�N
�� ��0)@▒  dev  (;▒�                                                                                                                                                                                                                                                                                                                                                                                                                                                                    
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls
fang-of-haynekhtnamet
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ 
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet  
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}
                                                                                                                                                                                                                                            
┌──(jars㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ 

```
## Notas adicionales
## Referencias 
