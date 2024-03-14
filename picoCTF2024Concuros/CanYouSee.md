## Objetivo
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/4/unknown.zip).
## Solución
```
elhakiao-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/4/unknown.zip
--2024-03-14 19:17:04--  https://artifacts.picoctf.net/c_titan/4/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252173 (2.1M) [application/octet-stream]
Saving to: 'unknown.zip'

unknown.zip                                                         100%[=================================================================================================================================================================>]   2.15M  --.-KB/s    in 0.02s   

2024-03-14 19:17:04 (99.4 MB/s) - 'unknown.zip' saved [2252173/2252173]

elhakiao-picoctf@webshell:~$ ls
README.txt  unknown.zip
elhakiao-picoctf@webshell:~$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
elhakiao-picoctf@webshell:~$ ls
README.txt  ukn_reality.jpg  unknown.zip
elhakiao-picoctf@webshell:~$ strings -n 10 ukn_reality.jpg 
7http://ns.adobe.com/xap/1.0/
<?xpacket begin='
' id='W5M0MpCehiHzreSzNTczkc9d'?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='Image::ExifTool 11.88'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'>
 <rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:attributionURL rdf:resource='cGljb0NURntNRTc0RDQ3QV9ISUREM05fZGVjYTA2ZmJ9Cg=='/>
 </rdf:Description>
</rdf:RDF>
</x:xmpmeta>
yZIevwv9ff9$
T=j2*U\/4]
="&rK09R:b
Y[      R/:UO2C
Y#|UU:m[CF
QV58,c{3mr
|9a(Qp  #zb
YgUUlEI&z\9
\c}7<XTt+'7k
<|ULf*-mvxXow
_:k6Oiy{o0
KCjSWF\92-l
/A[rZ0V"sRu5
%' sY5$wBJ
[y-|Guq<B9wM
2<sNcMSNqJ
]57*JNQmk+
W8xRj}ORir
\<:S_YO28"
{ewqi{  2Cy
R~cKGcz}NG
N|5|vn  <'p
I,5VKHnRk#
Rzw O2uESZ)
fNz{Uxp%#5#
XEmmzf78>n
2I`s,=ey)F
W{mcqigwmo
agkECD~sW.
Nm99K_$jx[R
r^K|>RR&~N2
T+t,A9S_Nx
},}<F;  :sMF
gm(bVF?7PqV
uvVR!hWn0H
XlJkG(=}N,
D0z)88`q]U
4A6(A+JW(M~'}
d!$VpZ-7:'-w:
F)6|^])KKmtA:
RiKOsV~B|G
S2\;c!s^^][
w)d8%OqPxl
;}E{9ENLLO
N^jSV_i]h|O
'sq[:` r*a
_1S=}j;KlH
rTb\9 Q99$J
*3rM;[_#;F
j>SVoXb?a]
v*3M+E+itA
kwqm{kqos$
.q\     jwNVDN0:TC
+E%KZ3BhPg
Y]GZ{9+N^T
J5*sZ*r=3U
F1jQOGfp`j
yIve&4n5)\
kB1>;4MWm+
TF2qR!5*.p;
Et=#+iuc(G
ZjwZs8w;k
elhakiao-picoctf@webshell:~$ strings -n 10 ukn_reality.jpg | grep pico
elhakiao-picoctf@webshell:~$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 12.40
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.2 MiB
File Modification Date/Time     : 2024:02:15 22:40:14+00:00
File Access Date/Time           : 2024:03:14 19:17:27+00:00
File Inode Change Date/Time     : 2024:03:14 19:17:12+00:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fZGVjYTA2ZmJ9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
picoCTF{ME74D47A_HIDD3N_deca06fb}
```
## Notas adicionales
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnROUlRjMFJEUTNRVjlJU1VSRU0wNWZaR1ZqWVRBMlptSjlDZz09
## Referencias
