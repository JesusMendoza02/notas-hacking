# Retos PicoCTF


## Objetivo 

Download this packet capture and find the flag.
Download packet capture
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ wget https://artifacts.picoctf.net/c/135/capture.flag.pcap
--2024-10-26 18:02:54--  https://artifacts.picoctf.net/c/135/capture.flag.pcap
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:be00:16:5ec5:2840:93a1, 2600:9000:25ed:a000:16:5ec5:2840:93a1, 2600:9000:25ed:5c00:16:5ec5:2840:93a1, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[2600:9000:25ed:be00:16:5ec5:2840:93a1]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 7518 (7.3K) [application/octet-stream]
Guardando como: “capture.flag.pcap”

capture.flag.pcap                     100%[======================================================================>]   7.34K  --.-KB/s    en 0s      

2024-10-26 18:02:54 (43.7 MB/s) - “capture.flag.pcap” guardado [7518/7518]

jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ wireshark capture.flag.pcap 
^Z
[1]+  Detenido                wireshark capture.flag.pcap
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ wireshark capture.flag.pcap &
[2] 22595
jesus@jesus-ThinkPad-T420:~/picoCTFjesus@jesus-ThinkPad-T420:~/picoCTF/sejesus@jesus-ThinkPad-T4jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123
Can't open file.des3 for reading, No such file or directory
140698388997440:error:02001002:system library:fopen:No such file or directory:../crypto/bio/bss_file.c:69:fopen('file.des3','rb')
140698388997440:error:2006D080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:76:
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ ls
capture.flag.pcap  file.des3  file.txt
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ cat file.txt 
picoCTF{nc_73115_411_0ee7267a}jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$ ^C
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/Eavesdrop$
```

## Notas adicionales 

## Referencias 
