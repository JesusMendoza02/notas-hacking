# Level 17 al Level 18


## Objetivo 
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit17**
passw
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

## Solución 
```bash
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ wc -l passwords.old
100 passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< bSrACvJvvBSxEM2SGsV5sn09vc3xgqyp
---
> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
bandit17@bandit:~$
```

## Notas adicionales
diff compara archivos de texto y muestra sus diferencias

## Referencias 
