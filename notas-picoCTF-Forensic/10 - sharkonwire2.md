# Retos PicoCTF


## Objetivo 

We found this packet capture. Recover the flag that was pilfered from the network.
## Solución 

```jesus@jesus-ThinkPad-T420:~$ pip install scapy
Defaulting to user installation because normal site-packages is not writeable
Collecting scapy
  Downloading scapy-2.6.0-py3-none-any.whl.metadata (5.6 kB)
Downloading scapy-2.6.0-py3-none-any.whl (2.4 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.4/2.4 MB 9.5 MB/s eta 0:00:00
Installing collected packages: scapy
Successfully installed scapy-2.6.0
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/forensic/
corrupt/          like1000/         sharkonwire2/     whitepages/
extensions/       moonwalk/         someta/           
gloryofthegarden/ sharkonwire1/     whatlieswithin/   
jesus@jesus-ThinkPad-T420:~$ cd picoCTF/forensic/sharkonwire2/
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sharkonwire2$ python3 exp.py 
  File "exp.py", line 9
    flag += char(p[UDP].sport - 5000})	
                                    ^
SyntaxError: closing parenthesis '}' does not match opening parenthesis '('
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sharkonwire2$ python3 exp.py 
Traceback (most recent call last):
  File "exp.py", line 9, in <module>
    flag += char(p[UDP].sport - 5000)	
NameError: name 'char' is not defined
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sharkonwire2$ python3 exp.py 
picoCTF{p1LLf3r3d_data_v1a_st3g0}
jesus@jesus-ThinkPad-T420:~/picoCTF/forensic/sharkonwire2$ 


from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''
for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000: 
                        flag += chr(p[UDP].sport - 5000)        


print(flag)






```

## Notas adicionales 

## Referencias 
 https://scapy.readthedocs.io/en/latest/introduction.html