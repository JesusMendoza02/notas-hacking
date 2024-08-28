# Retos Bandit 

# Level 8 al Level 9

## Objetivo 

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit8**
passw
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

## Solución 
```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
bandit8@bandit:~$
```

## Notas adicionales
Busca la palabra unica, pero primero los ordena para poder buscar las coincidencias
## Referencias 
https://www.geeksforgeeks.org/uniq-command-in-linux-with-examples/