# Retos Bandit 

# Level 9 al Level 10

## Objetivo 

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit9**
passw
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

## Solución 
```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ grep -a -o '==.*' data.txt 
========== the
========== passwordf
========== isc׃
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
bandit9@bandit:~$
```

## Notas adicionales
se busca que tuviera con grep en un archivo binario, yque solo muestre las coinicdencias muestre donde tenga varios ==
## Referencias 
es.linux-console.net/?p=15045