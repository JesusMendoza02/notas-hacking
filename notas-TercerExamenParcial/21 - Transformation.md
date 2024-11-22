# Retos PicoCTF


## Objetivo 

I wonder what this really is... [enc](https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solución 

```
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/transformation]
└─$ python3                    
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> enc=open("enc").read()
>>> print(enc)
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸弲㘶㠴挲ぽ
>>> for c in enc:
...     print(hex(ord(c)).lstrip("0x"),enc='')
... 
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
TypeError: 'enc' is an invalid keyword argument for print()
>>> for c in enc:
...     print(hex(ord(c)).lstrip("0x"),end='')
... 
7069636f4354467b31365f626974735f696e73743334645f6f665f385f32363638346332307d>>> 
>>> picoCTF{16_bits_inst34d_of_8_26684c20}

```

## Notas adicionales 

## Referencias 
