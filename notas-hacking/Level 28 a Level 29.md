# Level 28 al Level 29

## Objetivo 

There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit28**
passw
Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## Solución 
```bash
bandit28@bandit:~$ mktemp -d
/tmp/tmp.JBJWrFhpIG
bandit28@bandit:~$ cd /tmp/tmp.JBJWrFhpIG
bandit28@bandit:/tmp/tmp.JBJWrFhpIG$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
Receiving objects: 100% (9/9), 802 bytes | 802.00 KiB/s, done.
Resolving deltas: 100% (2/2), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
bandit28@bandit:/tmp/tmp.JBJWrFhpIG$ ls
repo
bandit28@bandit:/tmp/tmp.JBJWrFhpIG$ cd repo/
bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ git log
commit 8cbd1e08d1879415541ba19ddee3579e80e3f61a (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    fix info leak

commit 73f5d0435070c8922da12177dc93f40b2285e22a
Author: Morla Porla <morla@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    add missing data

commit 5f7265568c7b503b276ec20f677b68c92b43b712
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:30 2024 +0000

    initial commit of README.md
bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ git checkout 5f7265568c7b503b276ec20f677b68c92b43b712
Note: switching to '5f7265568c7b503b276ec20f677b68c92b43b712'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 5f72655 initial commit of README.md
bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: <TBD>

bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ git checkout 73f5d0435070c8922da12177dc93f40b2285e22a
Previous HEAD position was 5f72655 initial commit of README.md
HEAD is now at 73f5d04 add missing data
bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

bandit28@bandit:/tmp/tmp.JBJWrFhpIG/repo$
```

## Notas adicionales

crear mktemp-d 
clonar repositorio git clone despues de host poner el puerto 2220
pide passw del nivel 28
regresar a un commit donde este la passw usar log para ver los cambios 
y checkout para hacer el cambio 
## Referencias 
