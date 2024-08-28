# Level 11 al Level 12

## Objetivo 

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit11**
passw
 dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Solución 
```bash
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ alias rot13="tr 'A-Za-z' 'N-ZA-Mn-za-m'"
bandit11@bandit:~$ rot13 data.txt
tr: extra operand ‘data.txt’
Try 'tr --help' for more information.
bandit11@bandit:~$ cat data.txt | rot13
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
bandit11@bandit:~$
```

## Notas adicionales
el archivo se tiene que rotar el archivo 13 veces en el alfabeto  asi que solo se crea un alias con el comando rot13 lo cual va a decodificar la contrasena y ya solo se hace cat y se aplica el rot13
## Referencias 
https://stackoverflow.com/questions/5442436/using-rot13-and-tr-command-for-having-an-encrypted-email-address