# Retos PicoCTF


## Objetivo 

 Download the disk image and use mmls on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Download disk image
Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2024-10-17 19:42:59--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:8400:16:5ec5:2840:93a1, 2600:9000:25ed:e800:16:5ec5:2840:93a1, 2600:9000:25ed:f600:16:5ec5:2840:93a1, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[2600:9000:25ed:8400:16:5ec5:2840:93a1]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 29714372 (28M) [application/octet-stream]
Guardando como: “disk.img.gz”

disk.img.gz                           100%[======================================================================>]  28.34M  9.53MB/s    en 3.0s    

2024-10-17 19:43:02 (9.53 MB/s) - “disk.img.gz” guardado [29714372/29714372]

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ ls
disk.img.gz
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ gzip -d disk.img.gz 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ ls
disk.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ file disk.img 
disk.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,190,50), startsector 2048, 202752 sectors
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sleuthkitintro$ nc saturn.picoctf.net 57622
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
picoCTF{mm15_f7w!}

```

## Notas adicionales 

## Referencias 
