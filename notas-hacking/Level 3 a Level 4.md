# Retos Bandit 

# Level 3 al Level 4

## Objetivo 

The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit3**
passw
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## Solución 
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ find
.
./...Hiding-From-You
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$
```

## Notas adicionales 
El archivo estaba oculto en la carpeta por lo cual busque con find para encontrarla y aplicarle el cat 
## Referencias 