
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
## Solución
```
  350  cd /opt
  351  sudo  git clone https://github.com/colaclanth/sstv.git\n
  352  cd sstv
  353  python setup.py install
  354  sudo python setup.py install
  355  cd ~
  356  ls
  357  cd picoCTF
  358  clear
  359  ls
  360  cd forensic/m00nwalk
  361  ls
  362  clear
  363  sstv -d message.wav -o resultado.png
  364  ls
  365  open resultado.png
                                  
Clone un repositorio
picoCTF{beep_boop_im_in_space}
```
## Notas adicionales
## Referencias  
https://github.com/colaclanth/sstv
 