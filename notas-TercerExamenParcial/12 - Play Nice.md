# Retos PicoCTF


## Objetivo 

Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 33686` [playfair.py](https://mercury.picoctf.net/static/aec5fd7b1ec96307c4eda752a3353f68/playfair.py)
## Solución 

```
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ nc mercury.picoctf.net 33686
Here is the alphabet: v60ufmk7edg4z13h2oyqa9ib58ntwxlrscjp
Here is the encrypted message: 4celvfdkoq5a0dx7pr40ifzctd8488
What is the plaintext message? wd9bukbspdtj7skd3kl8d6oa3f03g0
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ nano playnice_solve.py      
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ nc mercury.picoctf.net 33686
Here is the alphabet: v60ufmk7edg4z13h2oyqa9ib58ntwxlrscjp
Here is the encrypted message: 4celvfdkoq5a0dx7pr40ifzctd8488
What is the plaintext message? dpksmue41bnyue84jlem2jhl9ux755
Congratulations! Here's the flag: 3a64de31e7b5acb6c87ae45050e187ee




┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ nano playnice_solve.py 
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ python playnice_solve.py 
now i= 0
now i= 2
now i= 4
now i= 6
now i= 8
now i= 10
now i= 12
now i= 14
now i= 16
now i= 18
now i= 20
now i= 22
now i= 24
now i= 26
now i= 28
dpksmue41bnyue84jlem2jhl9ux755
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/playnice]
└─$ 


```

## Notas adicionales 

## Referencias 
