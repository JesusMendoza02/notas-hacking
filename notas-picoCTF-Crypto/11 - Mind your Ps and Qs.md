# Retos PicoCTF


## Objetivo 


## Solución 

``` bash
>>> c = 8533139361076999596208540806559574687666062896040360148742851107661304651861689
>>> p = 1617549722683965197900599011412144490161
>>> q = 475693130177488446807040098678772442581573
>>> tn = (p-1)*(q-1)
>>> d = pow(e, -1,tn)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'e' is not defined
>>> e = 65537
>>> d = pow(e, -1,tn)
>>> m = (c ,d ,n)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined
>>> m = pow(c ,d ,n)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined
>>> n = p*q
>>> m = pow(c ,d ,n)
>>> m
13016382529449106065927291425342535437996222135352905256639629442503647501498237
>>> bytes.fromhex(hex(m)[2:]).decode()
'picoCTF{sma11_N_n0_g0od_45369387}'

```

## Notas adicionales 

## Referencias 
