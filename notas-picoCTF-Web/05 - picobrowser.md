# Retos PicoCTF


## Objetivo 

This website can be rendered only by picobrowser, go and catch the flag! https://jupiter.challenges.picoctf.org/problem/26704/ (link) or http://jupiter.challenges.picoctf.org:26704
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ curl -s https://jupiter.challenges.picoctf.org/problem/26704/flag -H 'User-Agent: picobrowser' | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}</code></p>
jesus@jesus-ThinkPad-T420:~$ 
```

## Notas adicionales 
You don't need to download a new web browser
## Referencias 
