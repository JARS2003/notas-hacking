## Objetivo
Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:54494/) to find the flag
## Solución




```
primero analisamos la pagina y encotramos que en la seccion de about nos dice que se puede encontrar la bandera en esta parte al anlizar el codigo fuente de la pagina encontramos que esta parte de codigo el cual el nofity true tiene algo que esta codeado

|   |
|---|
|<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMWY4MzI2MTV9">|
||<h1>|
||Try inspecting the page!! You might find it there|
||</h1>|
||<!-- .about-container -->|


despues solamente nos vamos a cyberchef y le decimos que la encode a base64 y nos da la contraseña

picoCTF{web_succ3ssfully_d3c0ded_1f832615}

```
## Notas adicionales

## Referencias 