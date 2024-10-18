# Retos PicoCTF


## Objetivo 

Download this disk image and find the flag.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Download compressed disk image
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ wget https://artifacts.picoctf.net/c/213/disk.flag.img.gz
--2024-10-17 20:00:58--  https://artifacts.picoctf.net/c/213/disk.flag.img.gz
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:b200:16:5ec5:2840:93a1, 2600:9000:25ed:c600:16:5ec5:2840:93a1, 2600:9000:25ed:d800:16:5ec5:2840:93a1, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[2600:9000:25ed:b200:16:5ec5:2840:93a1]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 44360922 (42M) [application/octet-stream]
Guardando como: “disk.flag.img.gz”

disk.flag.img.gz                      100%[======================================================================>]  42.31M  8.98MB/s    en 4.8s    

2024-10-17 20:01:03 (8.81 MB/s) - “disk.flag.img.gz” guardado [44360922/44360922]

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ gzip -d disk.flag.img.gz 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ file disk.flag.img 
disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x19,159,6), startsector 206848, 204800 sectors; partition 3 : ID=0x83, start-CHS (0x19,159,7), end-CHS (0x32,253,11), startsector 411648, 407552 sectors
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ ls
disk.flag.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ file disk.flag.img 
disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x19,159,6), startsector 206848, 204800 sectors; partition 3 : ID=0x83, start-CHS (0x19,159,7), end-CHS (0x32,253,11), startsector 411648, 407552 sectors
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ ls -la disk.flag.img 
-rw-rw-r-- 1 jesus jesus 419430400 mar 15  2023 disk.flag.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ fls -o  411648  disk.flag.img 
d/d 11:	lost+found
d/d 12:	boot
d/d 13:	etc
d/d 81:	proc
d/d 82:	dev
d/d 83:	tmp
d/d 84:	lib
d/d 87:	var
d/d 96:	usr
d/d 106:	bin
d/d 120:	sbin
d/d 460:	home
d/d 466:	media
d/d 470:	mnt
d/d 471:	opt
d/d 472:	root
d/d 473:	run
d/d 475:	srv
d/d 476:	sys
d/d 2041:	swap
V/V 51001:	$OrphanFiles
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ fls -o  411648  disk.flag.img 472
r/r 1875:	.ash_history
r/r * 1876(realloc):	flag.txt
r/r 1782:	flag.txt.enc
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ icat -o 411648 disk.flag.img 1782
Salted__�ށ��e��B�J�c�$QE&$��4jM�KGeE�1�^Ȥ7� ���؎$�'%jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ icat -o 411648 disk.flag.img 1782 > flag.txt.enc
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ file flag.txt.enc 
flag.txt.enc: openssl enc'd data with salted password
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ fls -o  411648  disk.flag.img 472
r/r 1875:	.ash_history
r/r * 1876(realloc):	flag.txt
r/r 1782:	flag.txt.enc
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ icat -o 411648 disk.flag.img 1875
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
Can't open flag.txt for reading, No such file or directory
140659117167936:error:02001002:system library:fopen:No such file or directory:../crypto/bio/bss_file.c:69:fopen('flag.txt','rb')
140659117167936:error:2006D080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:76:
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
140013807117632:error:06065064:digital envelope routines:EVP_DecryptFinal_ex:bad decrypt:../crypto/evp/evp_enc.c:610:
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$ cat flag.txt
picoCTF{h4un71ng_p457_5113beab}jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationorchid$
```

## Notas adicionales 

## Referencias 
