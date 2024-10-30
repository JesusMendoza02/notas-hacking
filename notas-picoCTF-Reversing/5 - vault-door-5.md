# Retos PicoCTF


## Objetivo 

In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: VaultDoor5.java
## Solución 

```
const expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm"
               + "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2"
               + "JTM0JTVmJTMwJTYyJTM5JTM1JTM3JTYzJTM0JTY2";


const finalResult = decodeURIComponent(decodeURIComponent(atob(expected)));

console.log(finalResult);

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_0b957c4f}
```

## Notas adicionales 

## Referencias 
