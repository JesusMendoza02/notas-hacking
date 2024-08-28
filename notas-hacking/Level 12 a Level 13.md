# Level 12 al Level 13

## Objetivo 

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit12**
passw
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## Solución 
```bash
bandit12@bandit:~$ cd /tmp/reto12a13
bandit12@bandit:/tmp/reto12a13$ mv data data.gz
bandit12@bandit:/tmp/reto12a13$ gzip -d data.gz
bandit12@bandit:/tmp/reto12a13$ ls
data
bandit12@bandit:/tmp/reto12a13$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/reto12a13$ mv data data.bz2
bandit12@bandit:/tmp/reto12a13$ bzip2 -d data.bz2
bandit12@bandit:/tmp/reto12a13$ ls
data
bandit12@bandit:/tmp/reto12a13$ file data
data: gzip compressed data, was "data4.bin", last modified: Wed Jul 17 15:57:06 2024, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/reto12a13$ mv data data.gz
bandit12@bandit:/tmp/reto12a13$ gzip -d data.gz
bandit12@bandit:/tmp/reto12a13$ ls
data
bandit12@bandit:/tmp/reto12a13$
bandit12@bandit:/tmp/reto12a13$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/reto12a13$ mv data data.tar
bandit12@bandit:/tmp/reto12a13$ tar xf data.tar
bandit12@bandit:/tmp/reto12a13$ ls
data5.bin  data.tar
bandit12@bandit:/tmp/reto12a13$ tar -xf data.tar
bandit12@bandit:/tmp/reto12a13$ ls
data5.bin  data.tar
bandit12@bandit:/tmp/reto12a13$ rm data.tar
bandit12@bandit:/tmp/reto12a13$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/reto12a13$ mv data5.bin data.tar
bandit12@bandit:/tmp/reto12a13$ tar xf data.tar
bandit12@bandit:/tmp/reto12a13$ ls
data6.bin  data.tar
bandit12@bandit:/tmp/reto12a13$ rm data.tar
bandit12@bandit:/tmp/reto12a13$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/reto12a13$ mv data6.bin data.bz2
bandit12@bandit:/tmp/reto12a13$ bzip2 -d data.bz2
bandit12@bandit:~$ cd /tmp/reto12a13
bandit12@bandit:/tmp/reto12a13$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/reto12a13$ mv data data.tar
bandit12@bandit:/tmp/reto12a13$ tar xf data.tar
bandit12@bandit:/tmp/reto12a13$ rm data.tar
bandit12@bandit:/tmp/reto12a13$ ls
data8.bin
bandit12@bandit:/tmp/reto12a13$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Wed Jul 17 15:57:06 2024, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/reto12a13$ mv data8.bin data.gz
bandit12@bandit:/tmp/reto12a13$ gzip -d data.gz
bandit12@bandit:/tmp/reto12a13$ ls
data
bandit12@bandit:/tmp/reto12a13$ file data
data: ASCII text
bandit12@bandit:/tmp/reto12a13$ cat data
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
bandit12@bandit:/tmp/reto12a13$
```

## Notas adicionales
El archivo esta en hexa asi que hay que decodificar para obtener la contraseña, entonces se busca en que tipo de archivo esta, y se descomprime ya que esta en bzip, entonces despues esta en gzip, despues en tar, despues en tar denuevo,  despues en bzip, en tar denuevo, y en gzip denuevo y ya se convierte en un ascii asi que ahora se aplica un cat para obtener la clave.
## Referencias 
