# Retos PicoCTF


## Objetivo 

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
## Solución 

```
                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm1]
└─$ wget 'https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt'
--2024-11-21 19:55:27--  https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 209 [application/octet-stream]
Saving to: ‘disassembler-dump0_a.txt’

disassembler-dump0_a 100%[======================>]     209  --.-KB/s    in 0s      

2024-11-21 19:55:27 (464 MB/s) - ‘disassembler-dump0_a.txt’ saved [209/209]

                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm1]
└─$ cat disassembler-dump0_a.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm1]
└─$ 
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm1]
└─$ python3         
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x30
48
>>> 

picoCTF{48}

```

## Notas adicionales 

## Referencias 
