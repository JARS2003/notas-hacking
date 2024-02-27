
## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
bandit29
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
## Solución
```
bandit29@bandit:~$ mkdir /tmp/jars29
bandit29@bandit:~$ cd /tmp/jars29
bandit29@bandit:/tmp/jars29$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
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
bandit29@bandit:/tmp/jars29$ ls
repo
bandit29@bandit:/tmp/jars29$ file repo/
repo/: directory
bandit29@bandit:/tmp/jars29$ cd repo/
bandit29@bandit:/tmp/jars29/repo$ ls
README.md
bandit29@bandit:/tmp/jars29/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/jars29/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/jars29/repo$ git branch   remotes/origin/sploits-dev
bandit29@bandit:/tmp/jars29/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/jars29/repo$ git branch -a
* dev
  master
  remotes/origin/sploits-dev
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/jars29/repo$  git checkout dev
Already on 'dev'
Your branch is up to date with 'origin/dev'.
bandit29@bandit:/tmp/jars29/repo$ ls
code  README.md
bandit29@bandit:/tmp/jars29/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/jars29/repo$
```
## Notas adicionales
El comando branch **te permite crear ramas de tu código, cambiarte y verlas**.
El comando git checkout  te permite desplazarte entre las ramas creadas por git branch
## Referencias 
https://github.com/richistron/aprendiendo-git/blob/master/docs/branch.md#:~:text=de%20tu%20codigo.-,El%20comando%20branch%20te%20permite%20crear,tu%20c%C3%B3digo%2C%20cambiarte%20y%20verlas.
https://www.atlassian.com/es/git/tutorials/using-branches/git-checkout#:~:text=El%20comando%20git%20checkout%20te,confirmaciones%20nuevas%20en%20dicha%20rama.