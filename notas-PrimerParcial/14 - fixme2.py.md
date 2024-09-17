# Retos PicoCTF


## Objetivo 

Fix the syntax error in the Python script to print the flag.
Download Python script
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ python3 fixme2.py 
  File "fixme2.py", line 22
    if flag = "":
            ^
SyntaxError: invalid syntax
jesus@jesus-ThinkPad-T420:~/Descargas$ nano fixme2.py 
jesus@jesus-ThinkPad-T420:~/Descargas$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
jesus@jesus-ThinkPad-T420:~/Descargas$
```

## Notas adicionales 

## Referencias 
