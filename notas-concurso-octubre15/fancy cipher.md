# Concurso CTF


## Objetivo 

Caesar isn't the only guy who can create good ciphers, mine is more fancy.
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ cd ConcuroCTFOct15/Crypto/
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/Crypto$ cd fancycipher/
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/Crypto/fancycipher$ nano fancy.py 
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/Crypto/fancycipher$ python3 fancy.py 
Shift: 198, Flag: flagmx{encryption_is_so_fancy}
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/Crypto/fancycipher
def decode(data, shift):
    dec = ''
    for _ in data:
        dec += chr((ord(_) - shift) % 0xff)
    return dec

cipher_text = '-3(.4?B,5*9@7;065&0:&:6&-(5*@D'

# Fuerza bruta para encontrar el shift correcto
for shift in range(256):
    decoded = decode(cipher_text, shift)
    if "flagmx" in decoded:
        print(f"Shift: {shift}, Flag: {decoded}")


```

## Notas adicionales 

## Referencias 
