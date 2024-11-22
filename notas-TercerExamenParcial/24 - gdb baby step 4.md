# Retos PicoCTF


## Objetivo 

`main` calls a function that multiplies `eax` by a constant. The flag for this challenge is that constant in decimal base. If the constant you find is 0x1000, the flag will be `picoCTF{4096}`. Debug [this](https://artifacts.picoctf.net/c/532/debugger0_d).
## Solución 

```
──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/gdbbabystep4]
└─$ python3 
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x3269
12905
>>> 

picoCTF{12905}
```

## Notas adicionales 

## Referencias 
