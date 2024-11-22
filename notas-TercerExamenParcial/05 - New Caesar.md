# Retos PicoCTF


## Objetivo 

We found a brand new type of encryption, can you break the secret code? (Wrap with picoCTF{}) `dcebcmebecamcmanaedbacdaanafagapdaaoabaaafdbapdpaaapadanandcafaadbdaapdpandcac` [new_caesar.py](https://mercury.picoctf.net/static/226a5ad9c9cb528673058d06d4c4380b/new_caesar.py)
## Solución 

```
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ cat new_caesar.py 
import string

LOWERCASE_OFFSET = ord("a")
ALPHABET = string.ascii_lowercase[:16]

def b16_encode(plain):
        enc = ""
        for c in plain:
                binary = "{0:08b}".format(ord(c))
                enc += ALPHABET[int(binary[:4], 2)]
                enc += ALPHABET[int(binary[4:], 2)]
        return enc

def shift(c, k):
        t1 = ord(c) - LOWERCASE_OFFSET
        t2 = ord(k) - LOWERCASE_OFFSET
        return ALPHABET[(t1 + t2) % len(ALPHABET)]

flag = "redacted"
key = "redacted"
assert all([k in ALPHABET for k in key])
assert len(key) == 1

b16 = b16_encode(flag)
enc = ""
for i, c in enumerate(b16):
        enc += shift(c, key[i % len(key)])
print(enc)
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ nano new_caesar_solve.py
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ python3 new_caesar_solve.py   
gbfefdfafcgdfefd
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ nano new_caesar_solve.py 
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ python3 new_caesar_solve.py
fdfcfefbfcfmfefbfefcfafmfcfmfafnfafefdfbfafcfdfafafnfafffafgfagpfdfafafofafbfafafafffdfbfagpfdgpfafafagpfafdfafnfafnfdfcfafffafafdfbfdfafagpfdgpfafnfdfcfafc
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ python3 new_caesar.py      
Traceback (most recent call last):
  File "/home/kali/picoCTF/retos/tercerparcial/newcaesar/new_caesar.py", line 21, in <module>
    assert all([k in ALPHABET for k in key])
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AssertionError
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ nano new_caesar_solve.py
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ python3 new_caesar_solve.py 
2A,AB
210? ,
!01ûó ñ/üôõþ/ýðÿô þ.ÿþòüü!ôÿ /þ.ü!ñ
/
/ ê
ëâàëãäíìïîãíîíáëëãîíëà
ÛÞÝÒÜß
Ü    ÝÜÐÚÚÒÝ
 Úß
ÈèÉÀýÎüÉÁÂËüÊÍÌÁýËûÌËÏÉÉþÁÌýüËûÉþÎ
íü×üý·×¸¿ì½ë¸°±ºë¹¼»°ìºê»º¾¸¸í°»ìëºê¸í½
ÜëÆëì¦Æ§®Û¬Ú§¯ ©Ú¨«ª¯Û©Ùª©­§§Ü¯ªÛÚ©Ù§Ü¬
ËÚµÚÛµÊÉÊÈËÊÉÈË
É¤ÉÊ¤¹¸¸¹·º¹¸·º
©¸¸¹st{¨y§t|}v§uxw|¨v¦wvztt©|w¨§v¦t©y
§§¨bcjhckledgfkefeicckfech
qQqRYWRZ[TSVUZTUTXRRZUTRW
v`@`AHuFtAIJCtBEDIuCsDCGAAvIDutCsAvF
et_tu?_07d5c0892c1438d2b32600e83dc2b0e5
TcNcd.N/&S$R/'(!R #"'S!Q"!%//T'"SR!Q/T$
CR=RS=BAAB@CBA@C
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ nano new_caesar_solve.py 
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/newcaesar]
└─$ 
picoCTF{et_tu?_07d5c0892c1438d2b32600e83dc2b0e5}
```

## Notas adicionales 

## Referencias 
