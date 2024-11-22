# Retos PicoCTF


## Objetivo 

Can you get the flag? Reverse engineer this [Python program](https://artifacts.picoctf.net/c/50/unpackme.flag.py).
## Solución 

```
                                                                                         
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackmepy]
└─$ ls
unpackme.flag.py
                                                                                           
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackmepy]
└─$ python unpackme.flag.py 
What's the password? asdasdas
That password is incorrect.
                                                                                           
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackmepy]
└─$ nano unpackme.flag.py 
                                                                                           
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/unpackmepy]
└─$ python unpackme.flag.py

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('picoCTF{175_chr157m45_85f5d0ac}')
else:
  print('That password is incorrect.')

```

## Notas adicionales 

## Referencias 
