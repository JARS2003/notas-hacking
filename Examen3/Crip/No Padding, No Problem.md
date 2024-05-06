## Objetivo
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 28517`.
## Solución
```
┌──(jars㉿jars)-[~/picoCTF/examen3/padd]
└─$ cat exp.py 
from pwn import *
import binascii

r = remote('mercury.picoctf.net', 28517)
r.recvlines(4)

r.recvuntil(b'n: ')
n = int(r.recvline().strip())

r.recvuntil(b'e: ')
e = int(r.recvline().strip())

r.recvuntil(b'ciphertext: ')
c = int(r.recvline().strip())

# Calculate payload
payload = c * pow(2,e,n)
r.sendlineafter(b'Give me ciphertext to decrypt: ', str(payload))

r.recvuntil(b'Here you go: ')
doubled_plain = int(r.recvline().strip())
print("Doubled Plain:", doubled_plain)

# Calculate plain text
plain_hex = hex(doubled_plain // 2)[2:]  # Remove '0x' prefix
plain_bytes = bytes.fromhex(plain_hex)
print("Plain Text Hex:", plain_hex)
print("Plain Text:", plain_bytes.decode())

r.close()                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/padd]
└─$ python exp.py
[+] Opening connection to mercury.picoctf.net on port 28517: Done
/home/jars/picoCTF/examen3/padd/exp.py:18: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendlineafter(b'Give me ciphertext to decrypt: ', str(payload))
Doubled Plain: 580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890769281669222390720762
Plain Text Hex: 7069636f4354467b6d347962335f54683073655f6d337335346733735f3472335f646966757272656e745f343030353533347d
Plain Text: picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_4005534}
[*] Closed connection to mercury.picoctf.net port 28517
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/examen3/padd]

```
## Notas adicionales
## Referencias 