# Retos PicoCTF


## Objetivo 

Download this disk image and find the flag.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Download compressed disk image
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ ls
disk.flag.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ fls -o 360448 disk.flag.img  -r

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ icat -o 360448 disk.flag.img 2363
apk add nano
mkdir my_folder
cd my_folder/
nano flag.txt
ls -al
iconv -f ascii -t utf16 > flag.uni.txt
l
ls -al
iconv -f ascii -t utf16 flag.txt > flag.uni.txt
ls -al
shred
shred -zu flag.txt 
ls -al
halt
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_adac6cb4}
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/SleuthkitApprentice$ 
```

## Notas adicionales 

## Referencias 
