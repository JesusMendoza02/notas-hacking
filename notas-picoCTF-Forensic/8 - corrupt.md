# Retos PicoCTF


## Objetivo 

We found this file. Recover the flag.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ ls
mystery
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ xxd mystery | head
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ hexeditor mystery 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ xxd mystery | head
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4322 4452  .PNG........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ hexeditor mystery 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ file mystery 
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ sidp apt install pngcheck

Orden «sidp» no encontrada. Quizá quiso decir:

  la orden «ssdp» del paquete snap «ssdp (0.0.1)»
  la orden «sipp» del paquete deb «sip-tester (1:3.6.0-1build1)»
  la orden «sip» del paquete deb «sip-dev (4.19.21+dfsg-1build1)»
  la orden «sfdp» del paquete deb «graphviz (2.42.2-3build2)»

Consulte «snap info <nombre del snap>» para ver más versiones.

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ sudo apt install pngcheck
[sudo] contraseña para jesus: 
Leyendo lista de paquetes... Hecho
Creando árbol de dependencias       
Leyendo la información de estado... Hecho
Se instalarán los siguientes paquetes NUEVOS:
  pngcheck
0 actualizados, 1 nuevos se instalarán, 0 para eliminar y 17 no actualizados.
Se necesita descargar 55.8 kB de archivos.
Se utilizarán 159 kB de espacio de disco adicional después de esta operación.
Des:1 http://mx.archive.ubuntu.com/ubuntu focal-updates/universe amd64 pngcheck amd64 2.3.0-7ubuntu0.20.04.1 [55.8 kB]
Descargados 55.8 kB en 1s (43.9 kB/s)                   
Seleccionando el paquete pngcheck previamente no seleccionado.
(Leyendo la base de datos ... 260831 ficheros o directorios instalados actualmente.)
Preparando para desempaquetar .../pngcheck_2.3.0-7ubuntu0.20.04.1_amd64.deb ...
Desempaquetando pngcheck (2.3.0-7ubuntu0.20.04.1) ...
Configurando pngcheck (2.3.0-7ubuntu0.20.04.1) ...
Procesando disparadores para man-db (2.9.1-1) ...
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ pngcheck -v mystery 
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ hexeditor mystery 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ file mystery 
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ pngcheck -v mystery 
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ hexeditor mystery 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ pngcheck -v mystery 
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ hexeditor mystery 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ pngcheck -v mystery 
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/corrupt$ 


picoCTF{c0rrupt10n_1847995}
```

## Notas adicionales 

## Referencias 
