# Retos Bandit 

# Level 4 al Level 5

## Objetivo 

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit4**
passw
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## Solución 
```bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ find
.
./-file00
./-file03
./-file08
./-file02
./-file04
./-file01
./-file07
./-file06
./-file05
./-file09
bandit4@bandit:~/inhere$ file
Usage: file [-bcCdEhikLlNnprsSvzZ0] [--apple] [--extension] [--mime-encoding]
            [--mime-type] [-e <testname>] [-F <separator>]  [-f <namefile>]
            [-m <magicfiles>] [-P <parameter=value>] [--exclude-quiet]
            <file> ...
       file -C [-m <magicfiles>]
       file [--help]
bandit4@bandit:~/inhere$ file -file00
file: Cannot open `ile00' (No such file or directory)
bandit4@bandit:~/inhere$ file -file01
file: Cannot open `ile01' (No such file or directory)
bandit4@bandit:~/inhere$ file -file02
file: Cannot open `ile02' (No such file or directory)
bandit4@bandit:~/inhere$ file -file03
file: Cannot open `ile03' (No such file or directory)
bandit4@bandit:~/inhere$ file -file04
file: Cannot open `ile04' (No such file or directory)
bandit4@bandit:~/inhere$ cat ./-file00
,YqfLj0x4Fbandit4@bandit:~/inhere$ cat ./-file01
N.bandit4@bandit:~/inhere$ cat ./-file02
9Fptk%bandit4@bandit:~/inhere$ cat ./-file03
nQy͍{+RbZkF* bandit4@bandit:~/inhere$ cat ./-file04

l]a߯-@gQ÷wzPߠybandit4@bandit:~/inhere$ cat ./-file05
pӻT9F3ˤ)
T՜Fǭbandit4@bandit:~/inhere$ cat ./-file06
QĹMp4-8=!#gbandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
bandit4@bandit:~/inhere$

```

##Notas adicionales
solo se podia leer el archivo 7 que contenia la contra

## Referencias 