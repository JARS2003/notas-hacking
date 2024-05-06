## Objetivo
keygenme-trial.py
## Solución
```
──(jars㉿jars)-[~/picoCTF/examen3/key]
└─$ code .                
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/key]
└─$ python exp.py
picoCTF{1n_7h3_|<3y_of_e584b363}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/key]
└─$ cat exp.py 
#!/usr/bin/env python3

import hashlib

username = b"SCHOFIELD"

key_prefix = "picoCTF{1n_7h3_|<3y_of_"

user_hash = hashlib.sha256(username).hexdigest()

key_prefix += user_hash[4]

key_prefix += user_hash[5]

key_prefix += user_hash[3]

key_prefix += user_hash[6]

key_prefix += user_hash[2]

key_prefix += user_hash[7]

key_prefix += user_hash[1]

key_prefix += user_hash[8]

key_prefix += "}"

print(key_prefix)
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/key]

```
## Notas adicionales
## Referencias 