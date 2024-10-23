# Retos PicoCTF


## Objetivo 

We found this weird message being passed around on the servers, we think we have a working decryption scheme.
Download the message here.
Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.
Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message})
## Solución 

```
>>> numeros = [165, 248, 94, 346, 299, 73, 198, 221, 313, 137, 205, 87, 336, 110, 186, 69, 223, 213, 216, 216, 177, 138]
>>> listacaracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
>>> caracteres = [listacaracteres[numeros % 37] for numero in numeros]
>>> ''.join(caracteres)
'R0UND_N_R0UND_B6B25531'
```

## Notas adicionales 

## Referencias 
