# Retos PicoCTF


## Objetivo 

Someone might have hidden the password in the trace file.
Find the key to unlock this file. This tracefile might be good to analyze.
## Solución 

```
This is the secret: picoCTF{R34DING_LOKd_
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/findandopen$ unzip flag.zip 
Archive:  flag.zip
[flag.zip] flag password: 
 extracting: flag                    
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/findandopen$ ls
dump.pcap  flag  flag.zip
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/findandopen$ cat flag
picoCTF{R34DING_LOKd_fil56_succ3ss_b98dda6a}
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/findandopen$ 

```

## Notas adicionales 

## Referencias 
