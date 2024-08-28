# Retos Bandit 

# Level 2 al Level 3

## Objetivo 

The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit2**
passw
263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## Solución 
```bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ find
.
./.bash_logout
./spaces in this filename
./.bashrc
./.profile
bandit2@bandit:~$ cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
bandit2@bandit:~$
```

## Notas adicionales 
 el nombre del archivo tenia espacios por lo cual solo tenia que ponerse comillas
## Referencias 
