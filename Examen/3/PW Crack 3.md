## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
en el .py agregue el for: 
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
for ps in pos_pw_list:
        level_3_pw_check(ps)
Y en el metodo comente la linea que pide la contraseña:
def level_3_pw_check(user_pw):
#    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
┌──(jars㉿kali)-[/tmp/jars]
└─$ nano level3.py  
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ nano level3.py 
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ python level3.py
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
                                                                                                                                                                                                                                           
┌──(jars㉿kali)-[/tmp/jars]
└─$ 


```
## Notas adicionales
## Referencias 