# Retos PicoCTF


## Objetivo 

Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 30048`.
## Solución 

```
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/nopaddingnoproblem]
└─$ nano nopad.py               
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/nopaddingnoproblem]
└─$ python3 nopad.py            
[+] Opening connection to mercury.picoctf.net on port 30048: Done
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:4: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("n:"))
b'Welcome to the Padding Oracle Challenge\nThis oracle will take anything you give it and decrypt using RSA. It will not accept the ciphertext with the secret message... Good Luck!\n\n\nn:'
103825943670608388724902101843105277664139778177296419807298638577533649838457681381229859055428873731297900741927275632463755233469715307082177465452101446353597897192597453744237913975978487031552964542799685433816426927633677765368693422819473428775571366017227037381835669466152304292930418647590777064957
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:7: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("e:"))
b'e:'
65537
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:10: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("ciphertext:"))
b'ciphertext:'
54782391385432962836155360736303300390029752693273674135830343335233109723211251809726621917561159210936912980512848055833305561357956651788963307455806191515914987192599986172752835236084199496591666317400246735952193832243744516176133029254377690684576826035080967557373951756878145853013927688003812920890
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:13: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("to decrypt:"))
b'\n\nGive me ciphertext to decrypt:'
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:14: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(str(pow(2,e,n)*c))
/home/kali/picoCTF/retos/tercerparcial/nopaddingnoproblem/nopad.py:15: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("you go:"))
b' Here you go:'
580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890769425795379846471930
290275030195850039473456618367455885069965748851278076756743720446703314517401359267322769037469251445384712897689923235965
b'picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_5052620}'
[*] Closed connection to mercury.picoctf.net port 30048
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/nopaddingnoproblem]





nopad.py
from pwn import *
import binascii
r=remote("mercury.picoctf.net", 30048)
print(r.recvuntil("n:"))
n=int(r.recvline())
print(n)
print(r.recvuntil("e:"))
e=int(r.recvline().strip())
print(e)
print(r.recvuntil("ciphertext:"))
c=int(r.recvline())
print(c)
print(r.recvuntil("to decrypt:"))
r.sendline(str(pow(2,e,n)*c))
print(r.recvuntil("you go:"))
p2=int(r.recvline())
print(p2)
print(p2//2)
st="{:x}".format(p2//2)
print(binascii.unhexlify(st))


```

## Notas adicionales 

## Referencias 
