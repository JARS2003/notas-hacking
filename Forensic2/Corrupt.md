## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Solución
```
──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ hexeditor mystery  
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ file mystery       
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ open mystery      
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ sudo apt install pngcheck          
[sudo] password for jars: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 1522 not upgraded.
Need to get 68.6 kB of archives.
After this operation, 208 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 pngcheck amd64 3.0.3-3 [68.6 kB]
Fetched 68.6 kB in 1s (128 kB/s)
Selecting previously unselected package pngcheck.
(Reading database ... 404457 files and directories currently installed.)
Preparing to unpack .../pngcheck_3.0.3-3_amd64.deb ...
Unpacking pngcheck (3.0.3-3) ...
Setting up pngcheck (3.0.3-3) ...
Processing triggers for man-db (2.12.0-1) ...
Processing triggers for kali-menu (2023.4.6) ...
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ pngcheck mystery 
mystery  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERROR: mystery
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ pngcheck -v mystery      
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ hexeditor mystery        
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ pngcheck -v mystery      
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ hexeditor mystery  
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ pngcheck -v mystery
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ hexeditor mystery  
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ pngcheck -v mystery
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]
└─$ open mystery             
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/forensic/corrupt]

picoCTF{c0rrupt10n_1847995}
```
## Notas adicionales
## Referencias 