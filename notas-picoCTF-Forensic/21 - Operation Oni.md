# Retos PicoCTF


## Objetivo 
Download this disk image, find the key and log into the remote machine.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Additional details will be available after launching your challenge instance.

## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ wget https://artifacts.picoctf.net/c/71/disk.img.gz
--2024-10-17 20:06:50--  https://artifacts.picoctf.net/c/71/disk.img.gz
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:5200:16:5ec5:2840:93a1, 2600:9000:25ed:a00:16:5ec5:2840:93a1, 2600:9000:25ed:2000:16:5ec5:2840:93a1, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[2600:9000:25ed:5200:16:5ec5:2840:93a1]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 48132743 (46M) [application/octet-stream]
Guardando como: “disk.img.gz”

disk.img.gz                           100%[======================================================================>]  45.90M  9.33MB/s    en 5.0s    

2024-10-17 20:06:56 (9.14 MB/s) - “disk.img.gz” guardado [48132743/48132743]

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ gzip -d disk.img.gz 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ ls
disk.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ fls -o 206848 disk.img 
d/d 11:	lost+found
d/d 12:	boot
d/d 13:	etc
d/d 79:	proc
d/d 80:	dev
d/d 81:	tmp
d/d 82:	lib
d/d 85:	var
d/d 94:	usr
d/d 104:	bin
d/d 118:	sbin
d/d 458:	home
d/d 464:	media
d/d 468:	mnt
d/d 469:	opt
d/d 470:	root
d/d 471:	run
d/d 473:	srv
d/d 474:	sys
V/V 33049:	$OrphanFiles
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ fls -o 206848 disk.img 470
r/r 2344:	.ash_history
d/d 3916:	.ssh
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ fls -o 206848 disk.img 3916
r/r 2345:	id_ed25519
r/r 2346:	id_ed25519.pub
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ icat -o 206848 disk.img 2344
ssh-keygen -t ed25519
ls .ssh/
halt
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ icat -o 206848 disk.img 2345 > key_file
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ chmod 600 key_file 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/operationoni$ ssh -i key_file -p 52316 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:52316 ([13.59.203.175]:52316)' can't be established.
ECDSA key fingerprint is SHA256:bAr5vzQiLGB7zQsjXlfTNpzZw4qLsrE39u6WXjqMjWA.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:52316,[13.59.203.175]:52316' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$ 

```

## Notas adicionales 

## Referencias 