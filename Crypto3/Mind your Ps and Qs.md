## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/cripto/psQs]
└─$ python
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> p = 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> q = 650809615742055581459820253356987396346063
>>> n = p*q
>>> tn = (p-1) * (q-1)
>>> e = 
KeyboardInterrupt
>>> e =65537
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> d = pow(e,-1,tn)
>>> m = pow(c,d,m)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'm' is not defined
>>> m = pow(c,d,n)
>>> m
301584840866101564855375427418886824758120417311086517597174699283280202343998247451898851614604920579884138166975740822740
>>> bytes.fromhex(hex(m)[2:])
b't\xca\x9f\xd9\xf1\x96\xf1\x00!R\x88R}k\xcf\x16\x95V\xcav\x0c\xe2A\x9e\xe0w\x08\xa8\x05{*\x18\xb3x\xadn\x9f\xee\xd2yn\xc3\x9a\xf7\x82&g\xe5\xe8\xc4\xd4'
>>> bytes.fromhex(hex(m)[2:])
b't\xca\x9f\xd9\xf1\x96\xf1\x00!R\x88R}k\xcf\x16\x95V\xcav\x0c\xe2A\x9e\xe0w\x08\xa8\x05{*\x18\xb3x\xadn\x9f\xee\xd2yn\xc3\x9a\xf7\x82&g\xe5\xe8\xc4\xd4'
>>> p =2434792384523484381583634042478415057961
>>> n = p*q
>>> tn = (p-1) * (q-1)
>>> d = pow(e,-1,tn)
>>> m = pow(c,d,n)
>>> bytes.fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_73918962}'
```
## Notas adicionales
## Referencias 