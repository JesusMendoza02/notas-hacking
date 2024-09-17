# Retos PicoCTF


## Objetivo 

I accidentally wrote the flag down. Good thing I deleted it!
You download the challenge files here:

## Solución 

```
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ ls
message.txt
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git status
En la rama master
nada para hacer commit, el árbol de trabajo está limpio
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git branch -a
* master
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git reflog
ef0b7cc (HEAD -> master) HEAD@{0}: commit: remove sensitive info
ea859bf HEAD@{1}: commit (initial): create flag
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git flag
git: 'flag' no es un comando de git. Mira 'git --help'.

El comando más similar es
	reflog
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git tag
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git log
commit ef0b7cc6b98367fa168573c931e0f7098ef59182 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    remove sensitive info

commit ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    create flag
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git checkout ef0b7cc6b98367fa168573c931e0f7098ef59182
Nota: cambiando a 'ef0b7cc6b98367fa168573c931e0f7098ef59182'.

Te encuentras en estado 'detached HEAD'. Puedes revisar por aquí, hacer
cambios experimentales y hacer commits, y puedes descartar cualquier
commit que hayas hecho en este estado sin impactar a tu rama realizando
otro checkout.

Si quieres crear una nueva rama para mantener los commits que has creado,
puedes hacerlo (ahora o después) usando -c con el comando checkout. Ejemplo:

  git switch -c <nombre-de-nueva-rama>

O deshacer la operación con:

  git switch -

Desactiva este aviso poniendo la variable de config advice.detachedHead en false

HEAD está ahora en ef0b7cc remove sensitive info
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ cat message.txt 
TOP SECRET
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ git checkout ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
La posición previa de HEAD era ef0b7cc remove sensitive info
HEAD está ahora en ea859bf create flag
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ 
jesus@jesus-ThinkPad-T420:~/Descargas/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_cf09a485}

```

## Notas adicionales 
git log: ver el historial de commits 
git checkout: cambiar al punto del commit que se le diga 
## Referencias 