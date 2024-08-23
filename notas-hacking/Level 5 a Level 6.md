# Retos Bandit 

# Level 5 al Level 6

## Objetivo 

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit5**
passw
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Solución 

bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere02  maybehere04  maybehere06  maybehere08  maybehere10  maybehere12  maybehere14  maybehere16  maybehere18
maybehere01  maybehere03  maybehere05  maybehere07  maybehere09  maybehere11  maybehere13  maybehere15  maybehere17  maybehere19
bandit5@bandit:~/inhere$ ls -la maybehere00
total 72
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 1039 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5  551 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 9388 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 7836 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 7378 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 4802 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 6118 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 6850 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 1915 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere01
total 80
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 6028 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 8944 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5  288 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 3070 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 9641 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 3792 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 4139 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 4543 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 8834 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere02
total 68
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 3801 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 6351 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 3511 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 2577 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 4932 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 7953 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 6746 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 8488 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 2275 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere03
total 80
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5  315 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 9769 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 6595 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 8880 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 8275 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 2282 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 2190 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 3385 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 9234 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere04
total 60
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 4410 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 2440 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 2619 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 6144 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 2117 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5  142 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 5532 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 2491 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 6002 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere05
total 64
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 2346 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 3201 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 5959 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 5917 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 2572 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 4585 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5  880 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 2420 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 8585 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere06
total 64
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 5731 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 1271 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 1076 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 8976 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 3443 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 2418 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 4073 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 4251 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 8065 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere07
total 56
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 3663 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 3065 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 2488 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5 1033 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 3362 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 1997 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5 4130 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 9064 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 1022 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ ls -la maybehere08
total 56
drwxr-x---  2 root bandit5 4096 Jul 17 15:57 .
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 ..
-rwxr-x---  1 root bandit5 1077 Jul 17 15:57 -file1
-rwxr-x---  1 root bandit5 8169 Jul 17 15:57 .file1
-rw-r-----  1 root bandit5 3825 Jul 17 15:57 -file2
-rw-r-----  1 root bandit5  747 Jul 17 15:57 .file2
-rwxr-x---  1 root bandit5 2650 Jul 17 15:57 -file3
-rwxr-x---  1 root bandit5 2217 Jul 17 15:57 .file3
-rwxr-x---  1 root bandit5  215 Jul 17 15:57 spaces file1
-rw-r-----  1 root bandit5 3693 Jul 17 15:57 spaces file2
-rwxr-x---  1 root bandit5 9138 Jul 17 15:57 spaces file3
bandit5@bandit:~/inhere$ cat .file2
cat: .file2: No such file or directory
bandit5@bandit:~/inhere$ cat maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        bandit5@bandit:~/inhere$
## Notas adicionales
se buscaba un archivo con 1033 bytes y que no fuera un ejecutable buscando en cada carpeta se encontro en la 07 en el archivo .file2

## Referencias 