# Retos PicoCTF


## Objetivo 

We found this file. Recover the flag.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ xxd -l 100 tunn3l_v1s10n 
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333                                0'#3
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ hexeditor tunn3l_v1s10n 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ eog tunn3l_v1s10n

(eog:4867): IBUS-WARNING **: 10:37:42.868: Unable to connect to ibus: No se pudo conectar: Conexión rehusada

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ exiftool tunn3l_v1s10n 
ExifTool Version Number         : 11.88
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.8 MB
File Modification Date/Time     : 2024:10:09 10:37:27-06:00
File Access Date/Time           : 2024:10:09 10:37:42-06:00
File Inode Change Date/Time     : 2024:10:09 10:37:27-06:00
File Permissions                : rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ hexeditor tunn3l_v1s10n 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/tunelvision$ eog tunn3l_v1s10n 

(eog:4919): IBUS-WARNING **: 10:40:21.497: Unable to connect to ibus: No se pudo conectar: Conexión rehusada

(eog:4919): EOG-WARNING **: 10:40:21.514: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita

picoCTF{qu1t3_a_v13w_2020}
```

## Notas adicionales 

## Referencias 
