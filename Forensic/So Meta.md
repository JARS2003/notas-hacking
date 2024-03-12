## Objetivo
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/forensic/SoMeta]
└─$ sudo apt install exiftool                                                                       
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Note, selecting 'libimage-exiftool-perl' instead of 'exiftool'
Suggested packages:
  libposix-strptime-perl
The following packages will be upgraded:
  libimage-exiftool-perl
1 upgraded, 0 newly installed, 0 to remove and 1526 not upgraded.
Need to get 3929 kB of archives.
After this operation, 289 kB of additional disk space will be used.
Get:1 http://http.kali.org/kali kali-rolling/main amd64 libimage-exiftool-perl all 12.76+dfsg-1 [3929 kB]
Fetched 3929 kB in 33s (118 kB/s)                 
(Reading database ... 399278 files and directories currently installed.)
Preparing to unpack .../libimage-exiftool-perl_12.76+dfsg-1_all.deb ...
Unpacking libimage-exiftool-perl (12.76+dfsg-1) over (12.67+dfsg-1) ...
Setting up libimage-exiftool-perl (12.76+dfsg-1) ...
Processing triggers for doc-base (0.11.1) ...
Processing 1 changed doc-base file...
Processing triggers for man-db (2.12.0-1) ...
Processing triggers for kali-menu (2023.4.6) ...
                                                                                                                    
┌──(jars㉿jars)-[~/picoCTF/forensic/SoMeta]
└─$ exiftool pico_img.png

ExifTool Version Number         : 12.76
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2020:10:26 12:38:23-06:00
File Access Date/Time           : 2024:03:12 12:27:26-06:00
File Inode Change Date/Time     : 2024:03:12 12:27:21-06:00
File Permissions                : -rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Warning                         : [minor] Text/EXIF chunk(s) found after PNG IDAT (may be ignored by some readers)
Artist                          : picoCTF{s0_m3ta_d8944929}
Image Size                      : 600x600
Megapixels                      : 0.360
                                                                                                                    
┌──(jars㉿jars)-[~/picoCTF/forensic/SoMeta]

```
## Notas adicionales
## Referencias 
