# Retos PicoCTF


## Objetivo 

Our flag printing service has started glitching!
Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ nc saturn.picoctf.net 53875
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
^C
jesus@jesus-ThinkPad-T420:~/Descargas$ nano script
jesus@jesus-ThinkPad-T420:~/Descargas$ python3 script.py 
picoCTF{gl17ch_m3_n07_a4392d2e}
jesus@jesus-ThinkPad-T420:~/Descargas$ 

```

## Notas adicionales 

## Referencias 
