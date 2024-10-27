# Retos PicoCTF


## Objetivo 

'Suspicious' is written all over this disk image. Download suspicious.dd.sda1
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/pitterpatters$ wget https://jupiter.challenges.picoctf.org/static/ca14d110858381cb297c1d22d62391a3/suspicious.dd.sda1
--2024-10-26 19:26:51--  https://jupiter.challenges.picoctf.org/static/ca14d110858381cb297c1d22d62391a3/suspicious.dd.sda1
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 32868864 (31M) [application/octet-stream]
Guardando como: “suspicious.dd.sda1”

suspicious.dd.sda1                    100%[======================================================================>]  31.35M  8.91MB/s    en 3.7s    

2024-10-26 19:26:56 (8.53 MB/s) - “suspicious.dd.sda1” guardado [32868864/32868864]

jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/pitterpatters$ strings -e b suspicious.dd.sda1 
dc7079dd_3<_|Lm_111t5_3b{FTCocip
qQWTYUiIOPb
FGjJKLs
ZXvc
#+3;CScs
!1Aa
qQWTYUiIOPb
FGjJKLs
ZXvc
#+3;CScs
!1Aa
#+3;CScs
!1Aa
7777777777
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/pitterpatters$ strings -e b suspicious.dd.sda1 | rev
picoCTF{b3_5t111_mL|_<3_dd9707cd
bPOIiUYTWQq
sLKJjGF
cvXZ
scSC;3+#
aA1!
bPOIiUYTWQq
sLKJjGF
cvXZ
scSC;3+#
aA1!
scSC;3+#
aA1!
7777777777
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/pitterpatters$ 
```

## Notas adicionales 

## Referencias 
