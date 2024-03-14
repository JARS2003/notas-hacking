## Objetivo
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)
## Solución
```
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/CommitmentIssues/drop-in]
└─$ git log                                                       
commit 3899edb7f3110d613c72ad40083fd8feeef703d0 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    remove sensitive info

commit 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    create flag
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/CommitmentIssues/drop-in]
└─$ git reflog 
3899edb (HEAD -> master) HEAD@{0}: commit: remove sensitive info
6603cb4 HEAD@{1}: commit (initial): create flag
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/CommitmentIssues/drop-in]
└─$ git show 3899edb^

commit 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    create flag

diff --git a/message.txt b/message.txt
new file mode 100644
index 0000000..ed59373
--- /dev/null
+++ b/message.txt
@@ -0,0 +1 @@
+picoCTF{s@n1t1z3_9539be6b}
                                                                                                                                                                                                                                           
┌──(jars㉿jars)-[~/picoCTF/retosEquipo/CommitmentIssues/drop-in]
└─$ 

```
## Notas adicionales
git log sirve para ver lo que se ha hecho en el repo.          
git reflog también para ver que se ha hecho pero esta solo muestra como el id para poder utilizarlo mas delante.
 git show 3899edb^ nos muestra el contenido del id que se nos dio anteriormente.
## Referencias 