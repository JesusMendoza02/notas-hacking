# Retos PicoCTF


## Objetivo 

Can you look at the data in this binary: static? This BASH script might help!
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ chmod +x static
jesus@jesus-ThinkPad-T420:~/Descargas$ chmod +x ltdis.sh 
jesus@jesus-ThinkPad-T420:~/Descargas$ ./ltdis.sh 
Attempting disassembly of  ...
objdump: 'a.out': No hay tal fichero
objdump: la sección '.text' se menciona en una opción -j, pero no se encuentra en ningún fichero de entrada
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
jesus@jesus-ThinkPad-T420:~/Descargas$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
jesus@jesus-ThinkPad-T420:~/Descargas$ grep picoCTF static.ltdis.strings.txt 
   1020 picoCTF{d15a5m_t34s3r_f6c48608}
jesus@jesus-ThinkPad-T420:~/Descargas$ 
```

## Notas adicionales 

## Referencias 
