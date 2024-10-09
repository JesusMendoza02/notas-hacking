# Retos PicoCTF


## Objetivo 

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: this
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/forensic/Matryoshkadoll/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg     
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll$ cd base_images/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images$ ls
2_c.jpg
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images$ unzip 2_c.jpg
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images$ cd base_images/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images/base_images$ unzip 3_c.jpg
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg     
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images/base_images$ cd base_images/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images/base_images/base_images$ unzip 4_c.jpg
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt                
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images/base_images/base_images$ ls
4_c.jpg  flag.txt
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/Matryoshkadoll/base_images/base_images/base_images$ cat flag.txt 
picoCTF{ac0072c423ee13bfc0b166af72e25b61}
```

## Notas adicionales 

## Referencias 
