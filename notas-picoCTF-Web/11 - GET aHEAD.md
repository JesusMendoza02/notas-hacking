# Retos PicoCTF


## Objetivo 

Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:53554/
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ curl -I http://mercury.picoctf.net:53554/
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
Content-type: text/html; charset=UTF-8

```

## Notas adicionales 
curl -I envia una solicitud HEAD 
## Referencias 
