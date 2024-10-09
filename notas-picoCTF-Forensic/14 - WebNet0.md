# Retos PicoCTF


## Objetivo 

We found this packet capture and key. Recover the flag.

## Solución 

```
picoCTF{nongshim.shrimp.crackers} 


Otra solucion 

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet0$ ssldump -r capture.pcap -k picopico.key -d | grep picoCTF
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet0$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
--
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet0$ 


```

## Notas adicionales 
se utiliza el wireshark, se ingresa la llave y aparecen las transacciones http, y ahi se ve la llave.
## Referencias 
