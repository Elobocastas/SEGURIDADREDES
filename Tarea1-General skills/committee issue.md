### 🚩 [- committee issue]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:


**Solución:** Aqui descargue la carpeta zip que habia en el sitio web luego la descomprimi 
`┌──(kali㉿kali)-[~/Downloads]
└─$ dir
Addadshashanammu      big-zip-files      challenge.zip  files.zip  level2.flag.txt.enc  level3.flag.txt.enc  level3.py  serpentine.py  strings
Addadshashanammu.zip  big-zip-files.zip  files          flag       level2.py            level3.hash.bin      ltdis.sh   static         warm
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
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
   creating: drop-in/.git/objects/d2/
 extracting: drop-in/.git/objects/d2/63841da2567e3e869d2b90e8e3bdd8838555b5  
   creating: drop-in/.git/objects/c0/
 extracting: drop-in/.git/objects/c0/cc0495794727db1682daa105367f28112796af  
   creating: drop-in/.git/objects/e7/
 extracting: drop-in/.git/objects/e7/20dc26a1a55405fbdf4d338d465335c439fb3e  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/a6/
 extracting: drop-in/.git/objects/a6/dca68e4310585eac3b5c9caf0f75967dfe972c  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
──(kali㉿kali)-[~/Downloads]
└─$ cat drop-in/message.txt 
TOP SECRET
`
- Luego investigue como hacer para ver las versiones de un archivo y fue con esto para dar con la bandera 
`┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git log -p               
commit a6dca68e4310585eac3b5c9caf0f75967dfe972c (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:06 2024 +0000

    remove sensitive info

diff --git a/message.txt b/message.txt
index d263841..d552d1e 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-picoCTF{s@n1t1z3_7246792d}
+TOP SECRET

commit e720dc26a1a55405fbdf4d338d465335c439fb3e
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:06 2024 +0000

    create flag

diff --git a/message.txt b/message.txt
new file mode 100644
index 0000000..d263841
--- /dev/null
+++ b/message.txt
@@ -0,0 +1 @@
+picoCTF{s@n1t1z3_7246792d}
`
**Referencias 
https://opensource-com.translate.goog/article/22/10/git-log-command?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=wa