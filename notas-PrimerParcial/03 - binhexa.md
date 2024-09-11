# Retos PicoCTF


## Objetivo 
Description
How well can you perfom basic binary operations?
Additional details will be available after launching your challenge instance.

## Solución 

```

jesus@jesus-ThinkPad-T420:~$ nc titan.picoctf.net 51471

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00000010
Binary Number 2: 10100010


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 000000100
Correct!

Question 2/6:
Operation 2: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10100100
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01010001
Correct!

Question 4/6:
Operation 4: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000010
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10100010
Correct!

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101000100
Correct!

Enter the results of the last operation in hexadecimal: 324
Incorrect answer!

Enter the results of the last operation in hexadecimal: 0x144

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}


```

## Notas adicionales 
se uso una calucladora de binarios para hacer las operaciones
## Referencias 
