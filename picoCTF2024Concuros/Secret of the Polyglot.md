## Objetivo
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf).
## Soluciòn
1. Al tratar de descargarlo se te abre como pdf y es la segunda parte de la llave
2. Para la primera solo se cambia la extension a png y al momento de abrir la imagen te aparece la primer parte


```
❯ ls
 forensic   discord-0.0.45.deb   discord-0.0.45.tar.gz   flag2of2-final.pdf
❯ mv flag2of2-final.pdf flag.png
❯ ls
 forensic   discord-0.0.45.deb   discord-0.0.45.tar.gz   flag.png
❯ open flag.png
```

picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}
