# Retos PicoCTF


## Objetivo 

Decode this message from the moon.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/moonwalk$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                  [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/moonwalk$ ls
message.wav  result.png


picoCTF{beep_boop_im_in_Space}
```

## Notas adicionales 
Se decodifica utilizando en sstv.
## Referencias 
https://github.com/colaclanth/sstv