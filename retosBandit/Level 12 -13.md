The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Objetivo
## Datos de acceso al nivel
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solución
```
bandit12@bandit:/tmp/35163175$ history
    1  clear
    2  ls
    3  cat data.txt
    4  clear
    5  ls -la
    6  xxd .profile
    7  clear
    8  xxd -r data.txt
    9  xxd -r data.txt | file -
   10  clear
   11  mkdir /tmp/35163175
   12  cd /tmp/35163175
   13  xxd -r ~/data.txt > data
   14  file data
   15  mv data.gz
   16  mv dat data.gz
   17  mv data data.gz
   18  gzip -d data.gz
   19  ls
   20  mv data data.bz2
   21  bzip2 -d data.bz2
   22  file data
   23  mv data data.gz
   24  gzip -d data.gz
   25  file data
   26  mv data data.tar
   27  tar xf data.tar
   28  ls
   29  rm data.tar
   30  file data5.bin
   31  mv data5.bin data5.tar
   32  tar xf data5.tar
   33  ls
   34  rm data.tar
   35  file data6.bin
   36  mv data6.bin data6.bz2
   37  ls
   38  bzip2 -d data6.bz2
   39  ls
   40  file data6
   41  mv data6 data6.tar
   42  ls
   43  tar xf data6.tar
   44  ls
   45  file data8
   46  file data8.bin
   47  mv data8.bin data8.zip
   48  ls
   49  mv data8.zip data8.gzip
   50  ls
   51  gzip -d data8.gzip
   52  history
bandit12@bandit:/tmp/35163175$ mv data8.gzip data8.gz
bandit12@bandit:/tmp/35163175$ gzip -d data8.gzip
gzip: data8.gzip.gz: No such file or directory
bandit12@bandit:/tmp/35163175$ gzip -d data8.gz
bandit12@bandit:/tmp/35163175$ ls
data5.tar  data6.tar  data8
bandit12@bandit:/tmp/35163175$ file data8
data8: ASCII text
bandit12@bandit:/tmp/35163175$ echo data8
data8
bandit12@bandit:/tmp/35163175$ strings data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:/tmp/35163175$
```
## Notas adicionales
## Referencias 
https://en.wikipedia.org/wiki/Hex_dump