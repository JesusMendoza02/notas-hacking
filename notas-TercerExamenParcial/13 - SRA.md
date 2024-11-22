# Retos PicoCTF


## Objetivo 

I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.
## Solución 

```
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/sra]
└─$ ls
chal.py  solve.py
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/sra]
└─$ nc saturn.picoctf.net 63852 
anger = 29639943937334012820708085492270611669609168533415137050399933456459905882204
envy = 29736386666635383822746372941687457146888338114024566385611056724651301928025
vainglory?
> 8u5zFxiuKV3983RA
8u5zFxiuKV3983RA
Conquered!
picoCTF{7h053_51n5_4r3_n0_m0r3_3858bd66}
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/sra]
└─$ 


┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/sra]
└─$ python3 solve.py    
anger = 29639943937334012820708085492270611669609168533415137050399933456459905882204
envy = 29736386666635383822746372941687457146888338114024566385611056724651301928025
['8u5zFxiuKV3983RA']
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/sra]
└─$ 


solve.py

```python
from Crypto.Util.number import isPrime, long_to_bytes
from string import ascii_letters, digits
from itertools import combinations
from sympy import divisors
from math import log2

anger = int(input("anger = "))
envy = int(input("envy = "))
sloth = 65537

ds = divisors(envy * sloth - 1)
primes = [x + 1 for x in ds if isPrime(x + 1)]
correct_size_primes = [x for x in primes if log2(x) // 1 == 127]

valid_plaintexts = []
charset = ascii_letters + digits
for p, q in combinations(correct_size_primes, 2):
    try:
        s = long_to_bytes(pow(anger, envy, p * q)).decode("ascii")
        if all([c in charset for c in s]):
            valid_plaintexts.append(s)
    except Exception:
        continue

print(valid_plaintexts)
```

```

## Notas adicionales 

## Referencias 
