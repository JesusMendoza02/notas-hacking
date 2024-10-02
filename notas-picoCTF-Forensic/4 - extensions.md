# Retos PicoCTF


## Objetivo 

This is a really weird text file TXT? Can you find the flag?
## Solución 

```bash
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ file flag.txt 
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ mv flag.txt flag.png
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ eog flag.png 

(eog:9772): EOG-WARNING **: 11:01:24.351: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ grep flag.png picoCTF
grep: picoCTF: No existe el archivo o el directorio
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ grep picoCTF flag.png 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ strings flag.png | grep picoCTF
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/extensions$ eog flag.png 

picoCTF{now_you_know_about_extensions}
```

## Notas adicionales 
file: para ver el tipo de archivo
mv para cambiar el tipo de extension 
## Referencias 
