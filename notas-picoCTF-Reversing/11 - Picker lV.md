# Retos PicoCTF


## Objetivo 

Can you figure out how this program works to get the flag?
Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/picker4$ ls
picker-IV  picker-IV.c
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/picker4$ nc saturn.picoctf.net 56950
Enter the address in hex to jump to, excluding '0x': ^C
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/picker4$ objdump -D picker-IV | grep win
000000000040129e <win>:
  4012d2:	75 16                	jne    4012ea <win+0x4c>
  4012f9:	eb 1a                	jmp    401315 <win+0x77>
  401319:	75 e0                	jne    4012fb <win+0x5d>
jesus@jesus-ThinkPad-T420:~/picoCTF/Reversing/picker4$ nc saturn.picoctf.net 56950
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

```

## Notas adicionales 

## Referencias 
