# Retos PicoCTF


## Objetivo 

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
You can download the challenge files here:

## Solución 

```
Primera parte
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git reflog
b4612c9 (HEAD, feature/part-2) HEAD@{0}: checkout: moving from 5c6d493ac583a95117d3a70eb5b10d9d76991c48 to b4612c9
5c6d493 (feature/part-3) HEAD@{1}: checkout: moving from main to 5c6d493
6ce09ad (main) HEAD@{2}: checkout: moving from feature/part-3 to main
5c6d493 (feature/part-3) HEAD@{3}: commit: add part 3
6ce09ad (main) HEAD@{4}: checkout: moving from main to feature/part-3
6ce09ad (main) HEAD@{5}: checkout: moving from feature/part-2 to main
b4612c9 (HEAD, feature/part-2) HEAD@{6}: commit: add part 2
6ce09ad (main) HEAD@{7}: checkout: moving from main to feature/part-2
6ce09ad (main) HEAD@{8}: checkout: moving from feature/part-1 to main
74ae521 (feature/part-1) HEAD@{9}: commit: add part 1
6ce09ad (main) HEAD@{10}: checkout: moving from main to feature/part-1
6ce09ad (main) HEAD@{11}: commit (initial): init flag printer
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git checkout 74ae521
La posición previa de HEAD era b4612c9 add part 2
HEAD está ahora en 74ae521 add part 1
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')

Segunda parte 
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git reflog
74ae521 (HEAD, feature/part-1) HEAD@{0}: checkout: moving from b4612c914d8461d1b1a50652cc303b76813ee142 to 74ae521
b4612c9 (feature/part-2) HEAD@{1}: checkout: moving from 5c6d493ac583a95117d3a70eb5b10d9d76991c48 to b4612c9
5c6d493 (feature/part-3) HEAD@{2}: checkout: moving from main to 5c6d493
6ce09ad (main) HEAD@{3}: checkout: moving from feature/part-3 to main
5c6d493 (feature/part-3) HEAD@{4}: commit: add part 3
6ce09ad (main) HEAD@{5}: checkout: moving from main to feature/part-3
6ce09ad (main) HEAD@{6}: checkout: moving from feature/part-2 to main
b4612c9 (feature/part-2) HEAD@{7}: commit: add part 2
6ce09ad (main) HEAD@{8}: checkout: moving from main to feature/part-2
6ce09ad (main) HEAD@{9}: checkout: moving from feature/part-1 to main
74ae521 (HEAD, feature/part-1) HEAD@{10}: commit: add part 1
6ce09ad (main) HEAD@{11}: checkout: moving from main to feature/part-1
6ce09ad (main) HEAD@{12}: commit (initial): init flag printer
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git checkout b4612c9
La posición previa de HEAD era 74ae521 add part 1
HEAD está ahora en b4612c9 add part 2
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')

Tercera parte 
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git reflog
b4612c9 (HEAD, feature/part-2) HEAD@{0}: checkout: moving from 74ae5215b93a82ddf3dd37df3d4c6b5aff0a93ed to b4612c9
74ae521 (feature/part-1) HEAD@{1}: checkout: moving from b4612c914d8461d1b1a50652cc303b76813ee142 to 74ae521
b4612c9 (HEAD, feature/part-2) HEAD@{2}: checkout: moving from 5c6d493ac583a95117d3a70eb5b10d9d76991c48 to b4612c9
5c6d493 (feature/part-3) HEAD@{3}: checkout: moving from main to 5c6d493
6ce09ad (main) HEAD@{4}: checkout: moving from feature/part-3 to main
5c6d493 (feature/part-3) HEAD@{5}: commit: add part 3
6ce09ad (main) HEAD@{6}: checkout: moving from main to feature/part-3
6ce09ad (main) HEAD@{7}: checkout: moving from feature/part-2 to main
b4612c9 (HEAD, feature/part-2) HEAD@{8}: commit: add part 2
6ce09ad (main) HEAD@{9}: checkout: moving from main to feature/part-2
6ce09ad (main) HEAD@{10}: checkout: moving from feature/part-1 to main
74ae521 (feature/part-1) HEAD@{11}: commit: add part 1
6ce09ad (main) HEAD@{12}: checkout: moving from main to feature/part-1
6ce09ad (main) HEAD@{13}: commit (initial): init flag printer
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git checkout 5c6d493
La posición previa de HEAD era b4612c9 add part 2
HEAD está ahora en 5c6d493 add part 3
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_4c24302f}")

```

## Notas adicionales 
git reflog: ver el historial de acciones en el repositorio 

## Referencias 
