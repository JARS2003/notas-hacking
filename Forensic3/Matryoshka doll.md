## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Solución
```

┌──(jars㉿jars)-[~/picoCTF/forensic/Matryoshka]
└─$ ls    
_dolls.jpg.extracted  dolls.jpg
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/picoCTF/forensic/Matryoshka]
└─$ cd _dolls.jpg.extracted 
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/picoCTF/forensic/Matryoshka/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/picoCTF/forensic/Matryoshka/_dolls.jpg.extracted]
└─$ open base_images  
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/picoCTF/forensic/Matryoshka/_dolls.jpg.extracted]
└─$ cd base_images         
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/forensic/Matryoshka/_dolls.jpg.extracted/base_images]
└─$ ls
2_c.jpg
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/forensic/Matryoshka/_dolls.jpg.extracted/base_images]
└─$ binwalk -e 2_c.jpg  

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/forensic/Matryoshka/_dolls.jpg.extracted/base_images]
└─$ ls
2_c.jpg  _2_c.jpg.extracted
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/forensic/Matryoshka/_dolls.jpg.extracted/base_images]
└─$ cd _2_c.jpg.extracted  
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/Matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls
2DD3B.zip  base_images
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/Matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images       
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg  _3_c.jpg.extracted
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted 
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ ls
1E2D6.zip  base_images
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images       
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd 4_c.jpg.extracted
cd: no such file or directory: 4_c.jpg.extracted
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ open 4_c.jpg    
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg  _4_c.jpg.extracted
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt
                                                                                                                                                                                                                                            
┌──(jars㉿jars)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt         
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}                                          

```
## Notas adicionales
## Referencias 