# Level 26 al Level 27

## Objetivo 

Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
cuenta
**bandit26**
passw
s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

## Solución 
```bash
C:\Users\Jesus>ssh -i key26.txt bandit26@bandit.labs.overthewire.org -p 2220
:set shell=/bien/bash
:shell 

bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB



C:\Users\Jesus>ssh -i key26.txt bandit26@bandit.labs.overthewire.org -p 2220
:set shell=/bien/bash
:shell 
bandit26@bandit:/tmp/tmp.U5dugjiItN$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Failed to add the host to the list of known hosts (/home/bandit26/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:

bandit26@bandit:/tmp/tmp.U5dugjiItN$ git clone ssh://bandit26-git@localhost:2220/home/bandit26-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Failed to add the host to the list of known hosts (/home/bandit26/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit26-git@localhost's password:
Permission denied, please try again.
bandit26-git@localhost's password:
Permission denied, please try again.
bandit26-git@localhost's password:
bandit26-git@localhost: Permission denied (publickey,password).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit26@bandit:/tmp/tmp.U5dugjiItN$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Failed to add the host to the list of known hosts (/home/bandit26/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:
Permission denied, please try again.
bandit27-git@localhost's password:
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit26@bandit:/tmp/tmp.U5dugjiItN$ ls
repo
bandit26@bandit:/tmp/tmp.U5dugjiItN$ cd repo/
bandit26@bandit:/tmp/tmp.U5dugjiItN/repo$ ls
README
bandit26@bandit:/tmp/tmp.U5dugjiItN/repo$ cat README
The password to the next level is: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN
bandit26@bandit:/tmp/tmp.U5dugjiItN/repo$
```

## Notas adicionales
ejecutar el bandit27do pero mandandole la pass de bandit27

## Referencias 
