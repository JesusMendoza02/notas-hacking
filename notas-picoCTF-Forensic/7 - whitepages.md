# Retos PicoCTF


## Objetivo 

I stopped using YellowPages and moved onto WhitePages... but the page they gave me is all blank!
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/moonwalk$ cd ..
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic$ mkdir whitepages
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic$ cd whitepages/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ wget https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt
--2024-10-08 20:15:41--  https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 2964 (2.9K) [application/octet-stream]
Guardando como: “whitepages.txt”

whitepages.txt                        100%[======================================================================>]   2.89K  --.-KB/s    en 0s      

2024-10-08 20:15:41 (97.0 MB/s) - “whitepages.txt” guardado [2964/2964]

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ ls
whitepages.txt
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ strings whitepages.txt | grep picoCTF
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ file whitepages.txt 
whitepages.txt: UTF-8 Unicode text, with very long lines, with no line terminators
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ 


from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)

print(data)

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/whitepages$ python3 exp.py 
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_c54f27cd05c2189f8147cc6f5deb2e56}\n\t\t'




```

## Notas adicionales 
powntools serie de librerias que facilitan el trabajo 
## Referencias 
