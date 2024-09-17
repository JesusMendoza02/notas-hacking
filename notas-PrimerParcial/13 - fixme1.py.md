# Retos PicoCTF


## Objetivo 

Fix the syntax error in this Python script to print the flag.
Download Python script
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ python3 fixme1.py 
  File "fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
    ^
IndentationError: unexpected indent
jesus@jesus-ThinkPad-T420:~/Descargas$ nano fixme1.py 
jesus@jesus-ThinkPad-T420:~/Descargas$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
jesus@jesus-ThinkPad-T420:~/Descargas$ 

```

## Notas adicionales 

## Referencias 
