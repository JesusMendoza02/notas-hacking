# Retos PicoCTF


## Objetivo 

We found this packet capture and key. Recover the flag.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ ls
capture.pcap  picopico.key
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2
    61 67 3a 20 70 69 63 6f 43 54 46 7b 74 68 69 73    ag: picoCTF{this
    2e 69 73 2e 6e 6f 74 2e 79 6f 75 72 2e 66 6c 61    .is.not.your.fla
    67 2e 61 6e 79 6d 6f 72 65 7d 0d 0a 43 6f 6e 74    g.anymore}..Cont
--
    67 3a 20 70 69 63 6f 43 54 46 7b 74 68 69 73 2e    g: picoCTF{this.
    69 73 2e 6e 6f 74 2e 79 6f 75 72 2e 66 6c 61 67    is.not.your.flag
    2e 61 6e 79 6d 6f 72 65 7d 0d 0a 43 6f 6e 74 65    .anymore}..Conte
--
    Pico-Flag: picoCTF{this.is.not.your.flag.anymore}
    Keep-Alive: timeout=5, max=99
    Connection: Keep-Alive
--
    00 00 00 01 00 00 00 01 70 69 63 6f 43 54 46 7b    ........picoCTF{honey.roasted.peanuts}......ICC_



--- otra forma --


jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ wireshark capture.pcap 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ ls
capture.pcap  picopico.key  vulture.jpg
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ eog vulture.jpg 

(eog:8851): IBUS-WARNING **: 11:17:22.900: Unable to connect to ibus: No se pudo conectar: Conexión rehusada

(eog:8851): EOG-WARNING **: 11:17:22.915: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ eog vulture.jpg 

(eog:8861): IBUS-WARNING **: 11:17:46.968: Unable to connect to ibus: No se pudo conectar: Conexión rehusada

(eog:8861): EOG-WARNING **: 11:17:46.983: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ strings vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/webnet1$ 

```

## Notas adicionales 

## Referencias 
