# Level 32 al Level 33

## Objetivo 
After all this `git` stuff, it’s time for another escape. Good luck!

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit32**
passw
3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K

## Solución 
```bash
WELCOME TO THE UPPERCASE SHELL
>> ls
sh: 1: LS: Permission denied
>> cat
sh: 1: CAT: Permission denied
>> $0
$ ls
uppershell
$ whoiam
sh: 2: whoiam: Permission denied
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0
$
```

## Notas adicionales

salir del upper con $0 
nos encontramos en bandit33
hacerle cat a la passw
## Referencias 
