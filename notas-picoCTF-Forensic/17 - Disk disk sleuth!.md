# Retos PicoCTF


## Objetivo 

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: dds1-alpine.flag.img.gz
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ sleuthkit
sleuthkit: no se encontró la orden
jesus@jesus-ThinkPad-T420:~$ sudo apt install /path/to/sleuthkit-version.
[sudo] contraseña para jesus: 
Leyendo lista de paquetes... Hecho
E: Se ha suministrado el fichero no admitido /path/to/sleuthkit-version. en la línea de órdenes
jesus@jesus-ThinkPad-T420:~$ sudo apt-get install sleuthkit
Leyendo lista de paquetes... Hecho
Creando árbol de dependencias       
Leyendo la información de estado... Hecho
sleuthkit ya está en su versión más reciente (4.6.7-1build1).
fijado sleuthkit como instalado manualmente.
0 actualizados, 0 nuevos se instalarán, 0 para eliminar y 31 no actualizados.
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/forensic/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic$ ls
corrupt     gloryofthegarden  MacroHardWeakEdge  milkslap  sharkonwire1  someta       webnet0  whatlieswithin
extensions  like1000          Matryoshkadoll     moonwalk  sharkonwire2  tunelvision  webnet1  whitepages
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic$ mkdir diskdisk
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic$ cd diskdisk/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ wget https://mercury.picoctf.net/static/626ea9c275fbd02dd3451b81f9c5e249/dds1-alpine.flag.img.gz
--2024-10-17 19:35:24--  https://mercury.picoctf.net/static/626ea9c275fbd02dd3451b81f9c5e249/dds1-alpine.flag.img.gz
Resolviendo mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Conectando con mercury.picoctf.net (mercury.picoctf.net)[18.189.209.142]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 29768910 (28M) [application/octet-stream]
Guardando como: “dds1-alpine.flag.img.gz”

dds1-alpine.flag.img.gz               100%[======================================================================>]  28.39M  8.25MB/s    en 3.4s    

2024-10-17 19:35:28 (8.25 MB/s) - “dds1-alpine.flag.img.gz” guardado [29768910/29768910]

jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ sudo apt-get install autopsy
Leyendo lista de paquetes... Hecho
Creando árbol de dependencias       
Leyendo la información de estado... Hecho
Se instalarán los siguientes paquetes NUEVOS:
  autopsy
0 actualizados, 1 nuevos se instalarán, 0 para eliminar y 31 no actualizados.
Se necesita descargar 326 kB de archivos.
Se utilizarán 1 046 kB de espacio de disco adicional después de esta operación.
Des:1 http://mx.archive.ubuntu.com/ubuntu focal/universe amd64 autopsy all 2.24-3 [326 kB]
Descargados 326 kB en 1s (309 kB/s)
Seleccionando el paquete autopsy previamente no seleccionado.
(Leyendo la base de datos ... 280334 ficheros o directorios instalados actualmente.)
Preparando para desempaquetar .../autopsy_2.24-3_all.deb ...
Desempaquetando autopsy (2.24-3) ...
Configurando autopsy (2.24-3) ...
Procesando disparadores para man-db (2.9.1-1) ...
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ file dds1-alpine.flag.img.gz 
dds1-alpine.flag.img.gz: gzip compressed data, was "dds1-alpine.flag.img", last modified: Tue Mar 16 00:20:04 2021, from Unix, original size modulo 2^32 134217728
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ gzip -d dds1-alpine.flag.img.gz 
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ ls
dds1-alpine.flag.img
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ file dds1-alpine.flag.img 
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ mmls dds1-alpine.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000262143   0000260096   Linux (0x83)
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$ srch_strings dds1-alpine.flag.img | grep picoCTF
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a6f4cab5}
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/diskdisk$
```

## Notas adicionales 

## Referencias 
