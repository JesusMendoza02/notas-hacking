# Level 29 al Level 30

## Objetivo 

There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit29**
passw
4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

## Solución 
```bash
bandit29@bandit:~$ mktemp -d
/tmp/tmp.kRAFQ6OTX1
bandit29@bandit:~$ cd /tmp/tmp.kRAFQ6OTX1
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1$ ls
repo
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1$ cd repo/
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ git log
commit efa5bd803f8335e5e5e9da5c4c7c876aefc9f8b4 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    fix username

commit 5a53eb83a43bac1f0b4e223e469b40ef68a4b6e6
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ git checkout master
Previous HEAD position was 5a53eb8 initial commit of README.md
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ git branch -a
  bandit29
  bandit30
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ git checkout dev
branch 'dev' set up to track 'origin/dev'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

bandit29@bandit:/tmp/tmp.kRAFQ6OTX1/repo$
```

## Notas adicionales

crear mktemp-d 
clonar repositorio git clone despues de host poner el puerto 2220
pide passw del nivel 29
se pasa a la rama master
se pasa a la rama dev
y se utiliza cat a readme
## Referencias 
