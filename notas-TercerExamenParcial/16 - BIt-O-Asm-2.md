# Retos PicoCTF


## Objetivo 

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución 

```
                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm2]
└─$ wget 'https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt'
--2024-11-21 19:59:23--  https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘disassembler-dump0_b.txt’

disassembler-dump0_b 100%[======================>]     270  --.-KB/s    in 0s      

2024-11-21 19:59:24 (23.4 MB/s) - ‘disassembler-dump0_b.txt’ saved [270/270]

                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm2]
└─$ cat disassembler-dump0_b.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret
                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm2]
└─$ 
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/bitoasm2]
└─$ python3
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x9fe1a
654874
>>> 

picoCTF{654874}

```

## Notas adicionales 

## Referencias 
