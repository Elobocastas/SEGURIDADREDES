### 🚩 [special]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

Start your instance to see connection details.

**Solución:** Primero entre a la direccion que me dieron con el ssh y  cuando quise poner un dir se me cambiaba y asi con cada comando entonces que manera habia sin utilizar caracteres strings y fue con carcateres que no pueda modificar 
`Special$ dir 
Dir 
sh: 1: Dir: not found
Special$ . ./*
. ./* 
Special$ . ./*/*
. ./*/* 
sh: 1: ./blargh/flag.txt: picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}: not found
Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
ELOBOCASTAS-academy@webshell:~$ `
`

**Referencias
https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html


