## Objetivo
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/66/challenge.zip)
## Solución
```
elhakiao-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/66/challenge.zip
--2024-03-14 19:05:39--  https://artifacts.picoctf.net/c_titan/66/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17740 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                                       100%[=================================================================================================================================================================>]  17.32K  --.-KB/s    in 0s      

2024-03-14 19:05:39 (72.8 MB/s) - 'challenge.zip' saved [17740/17740]

elhakiao-picoctf@webshell:~$ ls
README.txt  challenge.zip
elhakiao-picoctf@webshell:~$ file challenge.zip 
challenge.zip: Zip archive data, at least v1.0 to extract, compression method=store
elhakiao-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/33/
 extracting: drop-in/.git/objects/33/39c144a0c78dc2fbd3403d2fb37d3830be5d94  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
elhakiao-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
elhakiao-picoctf@webshell:~$ file drop-in 
drop-in: directory
elhakiao-picoctf@webshell:~$ cd drop-in/
elhakiao-picoctf@webshell:~/drop-in$ ls
message.txt
elhakiao-picoctf@webshell:~/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...elhakiao-picoctf@webshell:~/drop-in$ git status
On branch master
nothing to commit, working tree clean
elhakiao-picoctf@webshell:~/drop-in$ git log

[1]+  Stopped                 git log
elhakiao-picoctf@webshell:~/drop-in$ 
```
## Notas adicionales

## Referencias
