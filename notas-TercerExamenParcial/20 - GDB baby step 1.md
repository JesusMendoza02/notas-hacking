# Retos PicoCTF


## Objetivo 

Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Disassemble [this](https://artifacts.picoctf.net/c/512/debugger0_a).
## Solución 

```
kali㉿kali)-[~/picoCTF/retos/tercerparcial/gdbbabystep1]
└─$ chmod +x debugger0_a
                                                                                    
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/gdbbabystep1]
└─$ gdb debugger0_a
GNU gdb (Debian 15.2-1) 15.2
Copyright (C) 2024 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from debugger0_a...
(No debugging symbols found in debugger0_a)
(gdb) break main
Breakpoint 1 at 0x1131
(gdb) run
Starting program: /home/kali/picoCTF/retos/tercerparcial/gdbbabystep1/debugger0_a 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x0000555555555131 in main ()
(gdb) n
Single stepping until exit from function main,
which has no line number information.
__libc_start_call_main (main=main@entry=0x555555555129 <main>, argc=argc@entry=1, 
    argv=argv@entry=0x7fffffffde08) at ../sysdeps/nptl/libc_start_call_main.h:74
warning: 74     ../sysdeps/nptl/libc_start_call_main.h: No such file or directory
(gdb) info registers eax
eax            0x86342             549698
(gdb) print $eax
$1 = 549698
(gdb) 

picoCTF{549698}

```

## Notas adicionales 

## Referencias 
