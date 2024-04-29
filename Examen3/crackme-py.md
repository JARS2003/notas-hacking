## Objetivo
crackme.py
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
└─$ 
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
└─$ open crackme.py 
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
└─$ [main 2024-04-29T19:04:25.250Z] update#setState idle
[main 2024-04-29T19:04:55.259Z] update#setState checking for updates
[main 2024-04-29T19:04:55.263Z] update#setState available for download
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
└─$ python crackme.py
What's your first number? 1
What's your second number? 2
The number with largest positive magnitude is 2
picoCTF{1|\/|_4_p34|\|ut_502b984b}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
└─$ cat crackme.py 
# Hiding this really important number in an obscure piece of code is brilliant!
# AND it's encrypted!
# We want our biggest client to know his information is safe with us.
bezos_cc_secret = "A:4@r%uL`M-^M0c0AbcM-MFE0d_a3hgc3N"

# Reference alphabet
alphabet = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~"



def decode_secret(secret):
    """ROT47 decode

    NOTE: encode and decode are the same operation in the ROT cipher family.
    """

    # Encryption key
    rotate_const = 47

    # Storage for decoded secret
    decoded = ""

    # decode loop
    for c in secret:
        index = alphabet.find(c)
        original_index = (index + rotate_const) % len(alphabet)
        decoded = decoded + alphabet[original_index]

    print(decoded)



def choose_greatest():
    """Echo the largest of the two numbers given by the user to the program

    Warning: this function was written quickly and needs proper error handling
    """

    user_value_1 = input("What's your first number? ")
    user_value_2 = input("What's your second number? ")
    greatest_value = user_value_1 # need a value to return if 1 & 2 are equal

    if user_value_1 > user_value_2:
        greatest_value = user_value_1
    elif user_value_1 < user_value_2:
        greatest_value = user_value_2

    print( "The number with largest positive magnitude is "
        + str(greatest_value) )



choose_greatest()
decode_secret(bezos_cc_secret)                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/crachme]
picoCTF{1|\/|_4_p34|\|ut_502b984b}
```
## Notas adicionales
## Referencias 