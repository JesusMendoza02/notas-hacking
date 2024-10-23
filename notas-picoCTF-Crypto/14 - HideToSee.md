# Retos PicoCTF


## Objetivo 

How about some hide and seek heh?
Look at this image here.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/hidetosee$ ls
atbash.jpg
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/hidetosee$ steghide --extract -sf atbash.jpg 
Anotar salvoconducto: 
anot� los datos extra�dos e/"encrypted.txt".
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/hidetosee$ ls
atbash.jpg  encrypted.txt
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/hidetosee$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_05y2z65z}
jesus@jesus-ThinkPad-T420:~/picoCTF/Crypto/hidetosee$ 
uso cyberchef 
picoCTF{atbash_crack_05b2a65a}
```

## Notas adicionales 

## Referencias 
