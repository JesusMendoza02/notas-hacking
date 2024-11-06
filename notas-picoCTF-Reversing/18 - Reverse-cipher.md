# Retos PicoCTF


## Objetivo 

We have recovered a binary and a text file. Can you reverse the flag.
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ cd /picoCTF/Reversing/reversecipher
bash: cd: /picoCTF/Reversing/reversecipher: No existe el archivo o el directorio
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/Reversing/reversecipher
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ nano script.py
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ python3 script.py 
  File "script.py", line 9
    if j&1 = 0:
           ^
SyntaxError: invalid syntax
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ nano script.py 
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ nano script.py 
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ python3 script.py 
  File "script.py", line 10
    flag += chr{ ord(rev[j]) -5}
               ^
SyntaxError: invalid syntax
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ nano script.py 
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ python3 script.py 
Traceback (most recent call last):
  File "script.py", line 14, in <module>
    flag += rev[24]
IndexError: string index out of range
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ nano script.py 
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ python3 script.py 
picoCTF{r3v3rs312528e05}
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/reversecipher$ 

codigo: 

rev = open("rev_this").read()
flag = ''

for i in range(8):
	flag += rev[i]


for j in range(8,24):
	if j&1 == 0:
		flag += chr( ord(rev[j]) -5)
	else: 
		flag += chr( ord(rev[j]) + 2)

flag += rev[23]

print(flag)




```

## Notas adicionales 

## Referencias 
