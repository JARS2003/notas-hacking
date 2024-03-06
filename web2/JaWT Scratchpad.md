
## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Solución
```
Primero obtengo la cookie jwt:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiamFycyJ9.15tnADoNkoyvqof7enmX2IFMThHTrIQggNKNFQb3_Ps
Desenciptamos y cambiamos por admin:
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.-vh-85mhRjMzTUsaJEWhgJwu-_EzDOy8zI0a9dik2Ww
Despues usamos un ataque de fuerza bruta, para obtener la contra y asi poder ponerla en el desencriptador, para asi obtener la contraseña:picoCTF{jawt_was_just_what_you_thought_1ca14548}
```
## Notas adicionales
## Referencias 
https://jwt.io/