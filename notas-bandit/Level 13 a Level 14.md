# Level 13 al Level 14

## Objetivo 

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit13**
passw
 FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## Solución 
```bash
bandit13@bandit:~$ ssh -i sshkey.private  bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).

bandit14@bandit:~$ ls
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$


```

## Notas adicionales
Tenemos la llave ssh de bandit 14 por lo cual podemos ingresar a partir del ssh y estando dentro de bandit14 ya podemos ver su password.
## Referencias 
https://help.ubuntu.com/community/SSH/OpenSSH/Keys