# Retos PicoCTF


## Objetivo 

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)
Start your instance to see connection details.
Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas$ ssh -p 55633 ctf-player@saturn.picoctf.net
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Tue Sep 17 13:54:15 2024 from 127.0.0.1
Special$ Clear
Clear 
sh: 1: Clear: not found
Special$ Clear & ls
Clear & is 
sh: 1: is: not found
sh: 1: Clear: not found
Special$ find .
Find . 
sh: 1: Find: not found
Special$ Clear & find .
Clear & find . 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_6a2763f6}Special$
```

## Notas adicionales 

## Referencias 
