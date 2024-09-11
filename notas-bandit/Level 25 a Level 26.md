# Level 25 al Level 26

## Objetivo 
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

> NOTE: if you’re a Windows user and typically use Powershell to `ssh` into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit25**
passw
iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

## Solución 
```bash
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
C:\Users\Jesus>ssh -i key26.txt bandit26@bandit.labs.overthewire.org -p 2220
:set shell=/bien/bash
:shell 
bandit26@bandit:~$ cat /etc/bandit_pass/bandit26
s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
bandit26@bandit:~$
 
```

## Notas adicionales
Estando en el more teclamos en v para ir a vi, una ves estamos ahi teclamos esc :set shell=/bin/bash despues :shell
## Referencias 
