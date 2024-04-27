## Objetivo
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/86/gdbme).Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
## Solución
```
Muestro el historial porque no me deja copiar lo que me aparece despues 
  927  wget https://artifacts.picoctf.net/c/86/gdbme
  928  cat gdbme
  929  cat gdbme | grep pico
  930  cat gdbme | grep "p"
  931  chmod +x gdbme\
  932  chmod +x gdbme
  933  gdb gdbme
  934  sudo apt install gdb        \n
  935  gdb gdbme
  936  cd picoCTF/reversing/amg
  937  chmod +x gdbme
  938  gdb gdbme
picoCTF{d3bugg3r_dr1v3_72bd8355}
```
## Notas adicionales
## Referencias 