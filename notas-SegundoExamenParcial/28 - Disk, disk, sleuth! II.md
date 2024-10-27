# Retos PicoCTF


## Objetivo 

All we know is the file with the flag is named `down-at-the-bottom.txt`... Disk image: [dds2-alpine.flag.img.gz](https://mercury.picoctf.net/static/aed64c508175df5fe23207c10e0e47e5/dds2-alpine.flag.img.gz)
## Solución 

```
fls -F -r dds2-alpine.flag.img -o 2048
icat ./dds2-alpine.flag.img -o 2048 18291
picoCTF{f0r3nslc4t0r_novl3_f5565e7b}
```

## Notas adicionales 

## Referencias 
