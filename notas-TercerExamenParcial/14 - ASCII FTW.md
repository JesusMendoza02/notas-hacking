# Retos PicoCTF


## Objetivo 

This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program. You can download the file from [here](https://artifacts.picoctf.net/c/506/asciiftw).
## Solución 

```
0x00001184      mov     byte [var_38h], 0x70 ; 'p'

0x00001188      mov     byte [var_37h], 0x69 ; 'i'

0x0000118c      mov     byte [var_36h], 0x63 ; 'c'

0x00001190      mov     byte [var_35h], 0x6f ; 'o'

0x00001194      mov     byte [var_34h], 0x43 ; 'C'

0x00001198      mov     byte [var_33h], 0x54 ; 'T'

0x0000119c      mov     byte [var_32h], 0x46 ; 'F'

0x000011a0      mov     byte [var_31h], 0x7b ; '{'

0x000011a4      mov     byte [var_30h], 0x41 ; 'A'

0x000011a8      mov     byte [var_2fh], 0x53 ; 'S'

0x000011ac      mov     byte [var_2eh], 0x43 ; 'C'

0x000011b0      mov     byte [var_2dh], 0x49 ; 'I'

0x000011b4      mov     byte [var_2ch], 0x49 ; 'I'

0x000011b8      mov     byte [var_2bh], 0x5f ; '_'

0x000011bc      mov     byte [var_2ah], 0x49 ; 'I'

0x000011c0      mov     byte [var_29h], 0x53 ; 'S'

0x000011c4      mov     byte [var_28h], 0x5f ; '_'

0x000011c8      mov     byte [var_27h], 0x45 ; 'E'

0x000011cc      mov     byte [var_26h], 0x41 ; 'A'

0x000011d0      mov     byte [var_25h], 0x53 ; 'S'

0x000011d4      mov     byte [var_24h], 0x59 ; 'Y'

0x000011d8      mov     byte [var_23h], 0x5f ; '_'

0x000011dc      mov     byte [var_22h], 0x33 ; '3'

0x000011e0      mov     byte [var_21h], 0x43 ; 'C'

0x000011e4      mov     byte [var_20h], 0x46 ; 'F'

0x000011e8      mov     byte [var_1fh], 0x34 ; '4'

0x000011ec      mov     byte [var_1eh], 0x42 ; 'B'

0x000011f0      mov     byte [var_1dh], 0x46 ; 'F'

0x000011f4      mov     byte [var_1ch], 0x41 ; 'A'

0x000011f8      mov     byte [var_1bh], 0x44 ; 'D'

0x000011fc      mov     byte [var_1ah], 0x7d ; '}'



picoCTF{ASCII_IS_EASY_3CF4BFAD}

```

## Notas adicionales 

## Referencias 
