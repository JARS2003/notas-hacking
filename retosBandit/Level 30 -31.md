
## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
bandit30
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
## Solución
```
bandit30@bandit:/tmp/jars30$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
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
bandit30@bandit:/tmp/jars30$ ls
repo
bandit30@bandit:/tmp/jars30$ cd r
-bash: cd: r: No such file or directory
bandit30@bandit:/tmp/jars30$ cd repo/
bandit30@bandit:/tmp/jars30/repo$ ls
README.md
bandit30@bandit:/tmp/jars30/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/jars30/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Feb 27 21:08 .
drwxrwxr-x 3 bandit30 bandit30 4096 Feb 27 21:07 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Feb 27 21:08 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Feb 27 21:08 README.md
bandit30@bandit:/tmp/jars30/repo$ git tag
secret
bandit30@bandit:/tmp/jars30/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/jars30/repo$
```
## Notas adicionales
 **git tag** permite tener un nombre que apunta a un commit, esto marcar un punto específico en la historia de un repositorio.
 git show. El comando git show puede **mostrar un objeto Git de una manera simple y legible por humanos**. Normalmente se usaría esto para mostrar la información sobre una etiqueta o un commit.
## Referencias 
https://platzi.com/clases/1557-git-github/19952-tags-y-versiones-en-git-y-github/#:~:text=%F0%9F%93%8C%20git%20tag%20permite%20tener,la%20historia%20de%20un%20repositorio.
https://git-scm.com/book/es/v2/Ap%C3%A9ndice-C%3A-Comandos-de-Git-Inspecci%C3%B3n-y-Comparaci%C3%B3n#:~:text=git%20show,con%20anotaciones%20en%20Etiquetas%20Anotadas.