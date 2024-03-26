## Objetivo
Download the packet capture file and use packet analysis software to find the flag.
## Solución
```
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examne2/packets]
└─$ file network-dump.flag.pcap 
network-dump.flag.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examne2/packets]
└─$ cat network-dump.flag.pcap       
�ò�k&Nar�J'��'�9E<P�@@��

�n#('�Զ���▒A�
���dk&Na��J'�9'��E<@@"�

#(�n�&��'�Է���*O�
h��Í��dk&Na`�B'��'�9E4P�@@��

�n#('�Է�&����▒9
���eh���k&Na;�~'��'�9EpP�@@ѳ

�n#('�Է�&���▒�▒u
���eh���p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ b 9 d 5 3 7 6 5 }
k&Naa�B'�9'��E4g�@@��

#(�n�&��'�����Ui
h��č��ep&Na(
            <'�9''��s

p&NaX
     *'��''�9�
'��s
p&Na28*'��''�9�

p&Na�;<'�9''��s
'�9�
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examne2/packets]
picoCTF{p4ck37_5h4rk_b9d53765}
```
## Notas adicionales
## Referencias 