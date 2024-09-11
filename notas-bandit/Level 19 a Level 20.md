# Level 19 al Level 20


## Objetivo 
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit19**
passw
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

## Solución 
```bash
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
bandit19@bandit:~$
```

## Notas adicionales
setuid: es un bit que se puede modificar en un ejecutable para darle permisos a un usuario especifico
El archivo te da permisos de ser otro usuario y en este caso te permite ser bandit20 para tomar su password
## Referencias 
[setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)