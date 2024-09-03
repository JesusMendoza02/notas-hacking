# Level 21 al Level 22

## Objetivo 
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**bandit.labs.overthewire.org**
cuenta
**bandit21**
passw
EeoULMCra2q0dSkYj561DX7s1CpBuOBt

## Solución 
```bash
bandit21@bandit:~$ ls /etc/cron.d
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  e2scrub_all  otw-tmp-dir  sysstat
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
bandit21@bandit:~$
```

## Notas adicionales
Cron Job en linux es una herramienta qu epermite programar y ejecutar sentencia especificas dentro de nuestro sistema operativo linux de forma automatica 
/etc/cron.d ahi ponemos los cron jobs, o dicho de otra forma, los archivos que quiero se ejecuten cada vez que arranca la computadora.
## Referencias 
https://guias.donweb.com/guia-completa-de-cron-job-en-linux/