# Retos PicoCTF


## Objetivo 

This vault uses ASCII encoding for the password. The source code for this vault is here: VaultDoor4.java
## Solución 

```
const myBytes = [
    106, 85, 53, 116, 95, 52, 95, 98,
    0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
    0o142, 0o131, 0o164, 63, 0o163, 0o137, 0o143, 0o61,
    '9'.charCodeAt(0), '4'.charCodeAt(0), 'f'.charCodeAt(0), '7'.charCodeAt(0),
    '4'.charCodeAt(0), '5'.charCodeAt(0), '8'.charCodeAt(0), 'e'.charCodeAt(0),
];

const result = String.fromCharCode(...myBytes);

console.log(result);

picoCTF{jU5t_4_bUnCh_0f_bYt3s_c194f7458e}
```

## Notas adicionales 

## Referencias 
