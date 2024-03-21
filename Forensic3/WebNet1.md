## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
```
TTP/1.1 200 OK

Date: Fri, 23 Aug 2019 16:27:04 GMT

Server: Apache/2.4.29 (Ubuntu)

Last-Modified: Fri, 23 Aug 2019 16:26:33 GMT

ETag: "112fb-590cb44f2cbe6"

Accept-Ranges: bytes

Content-Length: 70395

Pico-Flag: picoCTF{this.is.not.your.flag.anymore}

Keep-Alive: timeout=5, max=99

Connection: Keep-Alive

Content-Type: image/jpeg

  

......JFIF..............Exif..MM.*.................J...........R.(...........;.........Z................................picoCTF{honey.roasted.peanuts}......ICC_PROFILE....
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet1]
└─$ open vulture.jpg 
                                                                                                                  
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet1]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
                                                                                                                  
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet1]
└─$ strings vulture.jpg | grep "pico"
picoCTF{honey.roasted.peanuts}
                                                                                                                  
┌──(jars㉿jars)-[~/picoCTF/forensic/WebNet1]
└─$ 

```
## Notas adicionales
## Referencias 