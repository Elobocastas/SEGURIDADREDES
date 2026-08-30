### 🚩 [-- - blame game]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
.Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)

You can download the challenge files here:


**Solución:**  Aqui igual descargue la carpeta que venia ,entre al directorio que era un archivo python ,intente leeerlo ,ejecutarlo y ver lo que contenia pero nada 
`──(kali㉿kali)-[~/Downloads/drop-in]
└─$ dir
message.py
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat message.py 
print("Hello, World!
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ python3 message.py 
  File "/home/kali/Downloads/drop-in/message.py", line 1
    print("Hello, World!"
 ^
SyntaxError: '(' was never closed
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ nano message.py 
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ python message.py 
Hello, World!

- Luego utilice el comando para ver el historial del archivo py  y un grep para encontrar mi bandera
` git log | grep picoCTF
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
Author: picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com>
Author: picoCTF <ops@picoctf.com>
`

``
`
`

[ picoCTF{@sk_th3_1nt3rn_e9957ce1}]

**Referencias
https://www.freecodecamp.org/espanol/news/explicacion-del-comando-git-log/


`