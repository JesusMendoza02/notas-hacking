# Retos PicoCTF


## Objetivo 

Can you get the flag?
Download this binary.
Here's the test drive instructions:
$ chmod +x gdbme
$ gdb gdbme
(gdb) layout asm
(gdb) break *(main+99)
(gdb) run
(gdb) jump *(main+104)
## Solución 


```
$ chmod +x gdbme
$ gdb gdbme
(gdb) layout asm
(gdb) break *(main+99)
Punto de interrupción 1 at 0x132a
(gdb) run
Starting program: /home/jesus/picoCTF/Reversing/gdbtestdrive/gdbme

Breakpoint 1, 0x000055555555532a in main ()
(gdb) jump *(main+104)
Continuando a 0x55555555532f.
picoCTF{d3bugg3r_dr1v3_72bd8355}
(gdb) ior 1 (process 10696) exited normally]


```

## Notas adicionales 

## Referencias 
