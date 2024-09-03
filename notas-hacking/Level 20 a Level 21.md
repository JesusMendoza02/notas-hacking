# Level 20 al Level 21


## Objetivo 
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit20**
passw
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

## Solución 
```bash
bandit20@bandit:~$ nc -lnvp 2222 <<< 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO &
[1] 3136561
bandit20@bandit:~$ Listening on 0.0.0.0 2222
^C
bandit20@bandit:~$ ./suconnect 2222
Connection received on 127.0.0.1 35450
Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
Password matches, sending next password
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
[1]+  Done                    nc -lnvp 2222 <<< 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
bandit20@bandit:~$
```

## Notas adicionales
&: si agregamos un simbolo de amperson al final del comando lo estamos enviando al segundo plano(background)
jobs: me muestra que comandos estan en el background
fg: saca un proceso o comando del segundo plano y lo trae al primer plano(foreground)
## Referencias 
