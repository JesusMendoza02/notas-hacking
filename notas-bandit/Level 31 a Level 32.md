# Level 31 al Level 32

## Objetivo 
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit31**
passw
fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

## Solución 
```bash
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ nano key.txt
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ nano key.txt
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git add .
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ cat .gitignore
*.txt
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ cat *.txt
May I come in?
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git status
HEAD detached at d83cd4d
nothing to commit, working tree clean
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ rm .gitignore
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git add key.txt
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git status
HEAD detached at d83cd4d
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   key.txt

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git commit -m ""
Aborting commit due to empty commit message.
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git commit -m "hola"
[detached HEAD 666e916] hola
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git push
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push origin HEAD:<name-of-remote-branch>

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git branch -a
* (HEAD detached from d83cd4d)
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git push -u
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push origin HEAD:<name-of-remote-branch>

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git checkout origin/
error: pathspec 'origin/' did not match any file(s) known to git
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git checkout HEAD
D       .gitignore
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git push
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push origin HEAD:<name-of-remote-branch>

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git status
HEAD detached from d83cd4d
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore

no changes added to commit (use "git add" and/or "git commit -a")
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git add key.txt
bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git push
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push origin HEAD:<name-of-remote-branch>

bandit31@bandit:/tmp/tmp.Y6MU51wabr/repo$ git push origin HEAD:master
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 319 bytes | 319.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] HEAD -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
```

## Notas adicionales

crear mktemp-d 
clonar repositorio git clone despues de host poner el puerto 2220
pide passw del nivel 31
se elimina el .gitignore
se crea key.txt y se envia a master
## Referencias 
