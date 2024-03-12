## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Solución
```
┌──(jars㉿jars)-[~]
└─$ mkdir picoCTF
                                                                             
┌──(jars㉿jars)-[~]
└─$ cd picoCTF 
                                                                             
┌──(jars㉿jars)-[~/picoCTF]
└─$ mkdir forensic
                                                                             
┌──(jars㉿jars)-[~/picoCTF]
└─$ cd forensic 
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic]
└─$ mkdir GloryoftheGarden 
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic]
└─$ cd GloryoftheGarden 
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2024-03-12 12:14:59--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[================>]   2.19M  1.68MB/s    in 1.3s    

2024-03-12 12:15:08 (1.68 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ ls
garden.jpg
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ file garden.jpg 
garden.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 2999x2249, components 3
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ open garden.jpg 
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ strings -n 10  garden.jpg
XICC_PROFILE
mntrRGB XYZ 
Copyright (c) 1998 Hewlett-Packard Company
sRGB IEC61966-2.1
sRGB IEC61966-2.1
IEC http://www.iec.ch
IEC http://www.iec.ch
.IEC 61966-2.1 Default RGB colour space - sRGB
.IEC 61966-2.1 Default RGB colour space - sRGB
,Reference Viewing Condition in IEC61966-2.1
,Reference Viewing Condition in IEC61966-2.1
        %       :       O       d       y
#*%%*525EE\
#*%%*525EE\
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
jVRVik#'        E
Kqk,*[zHW s
.n"Vg`8,2Mz
+^+}N/}7-^
(.Zm')[M_n
kHlmmWlpg/
@:W7ykc<RK4j
h       wvgpZ%!T
oKlqv6QYZy
jO$Q\oe8!G
{We:qN)-Zvf
z;7^}k,6        8:|
.ji[[&cF4qU
fU$P>Rx?J-
 ,J?!^ouyd
|f]8{hJVJ)
}>g<\gn_u5{4x
DVF?t7<}=+
l[Muyqp&#m
zxjRi9Is~F
=GcQZY^Egh
#<m;q^m_iZ
Y|Soif&YFQO=95
.fkBx'"Bx@
VrjN2I'm69
+Fpi>^[[]N
[Gq     ;x9*{WC{
5yo/$YJF0v
m6%bq{*ztM
_;$Mo#FF0F+
l5{mWOh/c*
F5      'r2     ,2=
vIidlkqJn7
yIn+v]N;M:T
'n~_SJm;->
zj0Z\XI8vL
bm.saewewlD
l=:IsB7rmI=w
I/-mr8<%bad
E9-m{_Vg7G
[\}Qn%[wo,
Fn+M7?N|Co
*y}-5VItW=7
cU*T_,uR]QX
<9yd53"\Aj
zx|5:Xx({h
Ksi#E2)a!=
qn;w<%,.nnv
kt}L15!E:p
_c^mHEUUoy]]_F
w{sog3m@8V+
Hn#7.70PS8;
_AQUsKk?=n]
Y=L4%)^I=-
3k$7[@|`tl
*D[X    0rFGj
)n%U`8$7j+
*E4RJC&FG'
su*(~$7z;^
OzWfwrN:VL
5:wZigm=w&
w:m_R7RDT`z
UZzkmu9eQ)=
hIINJ1Q[kgc
}7;=rdk[ub
Z2.]NGpONM:
BkR>i!>iB=
IpWTKFT$)8
M=u4wi'&Cif
=1H"#b0',8
hlk7pi6?iwL
aa,yD=E}..
3`|9pu]F9~C3
6RHK>e\oB:g
v0,'x^D99]
}4s,5'*x,<.
Fquau);^=l|
Pj2Oe2M:DR<
%F7}3_)x        u
*}r=sNFK}.e#
mN5'MBNPm?
09>WE:1NMiRz
ZRikwmum#|5iS
Y#B|+4;AlK ]
o<S#yrG dld
pEtN.mm.mle
\GhZY?y'oA
6L4n>R;r}+
wae:uc(>YwG
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
                                                                             
┌──(jars㉿jars)-[~/picoCTF/forensic/GloryoftheGarden]
└─$ strings -n 10  garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```
## Notas adicionales
## Referencias 