# Retos PicoCTF


## Objetivo 

Can you get the flag? Reverse engineer this [binary](https://artifacts.picoctf.net/c/203/unpackme-upx).
## Solución 

```
┌──(kali㉿kali)-[~]
└─$ python3                                                                   
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0xb83cb
754635
>>> exit()
                                                                                           
┌──(kali㉿kali)-[~]
└─$ cd picoCTF/retos/tercerparcial/unpackme 
                                                                                           
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackme]
└─$ ./           
                                                                                           
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackme]
└─$ ./unpackme-upx 
What's my favorite number? 754635
picoCTF{up><_m3_f7w_77ad107e}

```

## Notas adicionales 

## Referencias 
