# Level 10 al Level 11

## Objetivo 

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit10**
passw
 FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

## Solución 
```
bandit10@bandit:~$ base64 -d <<< data.txt
uZbase64: invalid input
bandit10@bandit:~$ openssl  base64 -d <<< data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ base64 -d <<< VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$
```

## Notas adicionales
El texto estaba en base64 entonces solo se tenia que decodificar
## Referencias 
https://www.baeldung.com/linux/cli-base64-encode-decode