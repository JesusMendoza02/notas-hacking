# Retos PicoCTF


## Objetivo 

This service can provide you with a random number, but can it do anything else?

Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/picker1$ nc saturn.picoctf.net 53724
Try entering "getRandomNumber" without the double quotes...
==> getRandomNumber
4
Try entering "getRandomNumber" without the double quotes...
==> win 
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x36 0x65 0x30 0x34 0x34 0x34 0x30 0x64 0x7d 
Try entering "getRandomNumber" without the double quotes...
==> 1
picoCTF{4_d14m0nd_1n_7h3_r0ugh_6e04440d}
```

## Notas adicionales 

## Referencias 
