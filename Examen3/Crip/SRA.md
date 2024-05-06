## Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...Connect to the program on our server: `nc saturn.picoctf.net 65451`Download the program: [chal.py](https://artifacts.picoctf.net/c/298/chal.py)
## Solución
```
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
    #initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
        #Generating sub list
        comb += [list(j) for j in combinations(l, i)]
    #Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
   #this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 65451)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
   #multiply them together to get p-1
   for k in l:
      product = product * k
   #if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
      #decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
         #see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue
┌──(diego㉿kali)-[~/Documents/picoCTF/Examen Parcial 3/SRA]
└─$ python exp.py 
[+] Opening connection to saturn.picoctf.net on port 65451: Done
/home/diego/Documents/picoCTF/Examen Parcial 3/SRA/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/diego/Documents/picoCTF/Examen Parcial 3/SRA/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 30463214957689220749046134890969046781556728098773664321754239433866451937191
d= 61259122016866778534047910020713751922062031307229807747990538527713413353925
/home/diego/Documents/picoCTF/Examen Parcial 3/SRA/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  4014739079619398064785897879027517159716179345781919910380055923490753970976182724
[2, 2, 3, 11, 71, 89, 719, 47653, 285983, 848993, 1903747, 4877911, 509553221, 6931791481, 13048072853, 1351907745662791]
{336733195325750584778968749875916542887, 202454838125411445379792679267857819507, 178629090640682958457277022571104399613, 239922381048915417435939612439379884399, 191501376271298289375031266316883923603, 327617075289499517503503727818010027583, 240459035240054708560431174634589637133, 333297336552123218068997404591226864207, 300338359770699537515490257753161542469, 256740951528499569792929592491422667437, 326314387539795522132926265610571517997, 232625146301332140220758364459310285767}
sKJ9qxMf3hinUwH7
/home/diego/Documents/picoCTF/Examen Parcial 3/SRA/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> sKJ9qxMf3hinUwH7\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}\r\n'
sKJ9qxMf3hinUwH7
[*] Closed connection to saturn.picoctf.net port 65451
```
## Notas adicionales
## Referencias 