# Level 14 al Level 15

## Objetivo 
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit14**
passw
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

## Solución 
```bash
bandit14@bandit:~$ which nc
/usr/bin/nc
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


```

## Notas adicionales
tenemos que conectaron al puerto 30000 de este nivel y de ahi mandarle la password del nivel actual para que de la password nueva
nc es  una herramienta que permite conectarse a un host remoto, tambien podemos abrir un puerto 

## Referencias 
https://www.ochobitshacenunbyte.com/2021/11/04/uso-del-comando-ncat-nc-en-linux-con-ejemplos/