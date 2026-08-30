### 🚩 [-- time machine]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:


**Solución:**  Aqui solo descargue la carpeta y la descomprimi y cuanbdo la descomprimi entre a la carpeta que tenia dentro 
`┌──(kali㉿kali)-[~/Downloads]
└─$ unzip challenge.zip 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd drop-in  
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ dir
message.txt
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                                                                                                                                                                                           
-Utilice un comando igual para que me de el historial del archivo y asi consegui la bandera
`┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git log
commit b92bdd8ec87a21ba45e77bd9bed3e4893faafd0f (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:29 2024 +0000

[picoCTF{t1m3m@ch1n3_5cde9075}
`



**Referencias
https://www.freecodecamp.org/espanol/news/explicacion-del-comando-git-log/


`