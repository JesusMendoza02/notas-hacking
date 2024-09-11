# Retos PicoCTF

## Objetivo 

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ unzip big-zip-files.zip
jesus@jesus-ThinkPad-T420:~/Descargas$ cd big-zip-files/
jesus@jesus-ThinkPad-T420:~/Descargas/big-zip-files$ grep -r picoCTF
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}```


```
## Notas adicionales 
unzip: sirve para descomprimir archivos con extencion zip
grep : busca un string en un archivo, al usar -r lo busca de manera recursiva dejandolo buscar dentro de carpetas
## Referencias 