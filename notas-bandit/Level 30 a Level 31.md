# Level 30 al Level 31

## Objetivo 
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit30**
passw
qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

## Solución 
```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.4l4AqjjhxK
bandit30@bandit:~$ cd /tmp/tmp.4l4AqjjhxK
bandit30@bandit:/tmp/tmp.4l4AqjjhxK$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit30@bandit:/tmp/tmp.4l4AqjjhxK$ cd repo/
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git checkout master
Already on 'master'
Your branch is up to date with 'origin/master'.
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git log
commit 60410f42e05023128098dc1f6991c75e6ae02e47 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:34 2024 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git checkout 60410f42e05023128098dc1f6991c75e6ae02e47
Note: switching to '60410f42e05023128098dc1f6991c75e6ae02e47'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 60410f4 initial commit of README.md
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git switch -c bandit31
Switched to a new branch 'bandit31'
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$ git show secret
fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
bandit30@bandit:/tmp/tmp.4l4AqjjhxK/repo$
```

## Notas adicionales

crear mktemp-d 
clonar repositorio git clone despues de host poner el puerto 2220
pide passw del nivel 30
se utiliza git tag para ver etiquetas y
con git show se muestra la etiqueta
## Referencias 
