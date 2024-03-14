## Objetivo
Description
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.
You can download the challenge files here:
challenge.zip
Additional details will be available after launching your challenge instance.

## Solución




```
ctf-player@pico-chall$ cat checksum.txt 
467a10447deb3d4e17634cacc2a68ba6c2bb62a6637dad9145ea673bf0be5e02
ctf-player@pico-chall$ sha256sum files/* | grep checksum.txt 
ctf-player@pico-chall$ sha256sum files/* | grep 467a10447deb3d4e17634cacc2a68ba6c2bb62a6637dad9145ea673bf0be5e02
467a10447deb3d4e17634cacc2a68ba6c2bb62a6637dad9145ea673bf0be5e02  files/c6c8b911
ctf-player@pico-chall$ 
Display all 642 possibilities? (y or n)
ctf-player@pico-chall$ ls
checksum.txt  decrypt.sh  files
ctf-player@pico-chall$ ./decrypt.sh files/c6c8b911
picoCTF{trust_but_verify_c6c8b911}
ctf-player@pico-chall$ Connection to rhea.picoctf.net closed by remote host.
Connection to rhea.picoctf.net closed.
                                                                                                                                                                                                                                            
┌──(aratt㉿kali)-[/tmp/…/home/ctf-player/drop-in/files]
└─$ 


```
## Notas adicionales

## Referencias 