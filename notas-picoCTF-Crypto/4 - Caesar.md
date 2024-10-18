# Retos PicoCTF


## Objetivo 

Decrypt this message.
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/Crypto/
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto$ ls
easy1  thenumbers
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto$ mkdir Caesar
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto$ cd C
bash: cd: C: No existe el archivo o el directorio
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto$ cd Caesar/
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/Caesar$ wget https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
--2024-10-17 20:23:13--  https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 35 [application/octet-stream]
Guardando como: “ciphertext”

ciphertext                            100%[======================================================================>]      35  --.-KB/s    en 0s      

2024-10-17 20:23:13 (1.24 MB/s) - “ciphertext” guardado [35/35]

jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/Caesar$ file ciphertext 
ciphertext: ASCII text, with no line terminators
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/Caesar$ cat ciphertext 
picoCTF{dspttjohuifsvcjdpoabrkttds}jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/Caesar$ ^C
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/Caesar$ 
se utiliza Cyberchef se utiliza root13 pero en 25 veces
picoCTF{crossingtherubiconzaqjsscr}

```

## Notas adicionales 

## Referencias 
