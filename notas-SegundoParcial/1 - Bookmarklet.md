# Retos PicoCTF


## Objetivo 

Why search for the flag when I can make a bookmarklet to print it for me?
Additional details will be available after launching your challenge instance.
## Solución 

```bash
javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£Ö�ÓÚåÛÑ¢ÕÓ�¨Í�ÕÄ¦�í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();

picoCTF{p@g3_turn3r_18d2fa20}
```

## Notas adicionales 

## Referencias 
