## Objetivo
A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?
## Solución
```
──(jars㉿jars)-[~/picoCTF/examen3/subs]
└─$ python exp.py
The flag is: picoCTF{5UB5717U710N_3V0LU710N_59533A2E}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/subs]
└─$ cat exp.py     
def decrypt_substitution_cipher(ciphertext, key):
    alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    decrypted_text = ""
    for char in ciphertext:
        if char.isalpha():
            # Obtener el índice del caracter en el alfabeto cifrado
            index = key.index(char.upper())
            # Usar el índice para obtener el caracter original del alfabeto
            original_char = alphabet[index]
            # Mantener la misma capitalización que el caracter original
            if char.islower():
                original_char = original_char.lower()
            decrypted_text += original_char
        else:
            decrypted_text += char
    return decrypted_text

# Ejemplo de uso
ciphertext = "Bif mwdy qa: xqcpCBM{5UE5717U710Z_3S0WU710Z_59533D2F}"                                                                                                                                                                                                                                         

key = "DECKFMYIQJRWTZPXGNABUSOLVH"
decrypted_message = decrypt_substitution_cipher(ciphertext, key)
print(decrypted_message)
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/subs]
└─$ 




```
## Notas adicionales
## Referencias 