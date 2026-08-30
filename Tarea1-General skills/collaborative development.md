### 🚩 [-- collaborative development]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/177/challenge.zip)

**Solución:**  aQUI descargue el archivo zip y lo descomprimi 
`┌──(kali㉿kali)-[~/Downloads]
└─$ unzip challenge.zip 
`┌──(kali㉿kali)-[~/Downloads]
└─$ cd drop-in           
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ dir
flag.py
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat flag.py         
print("Printing the flag...")  
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ nano flag.py     
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git log | grep picoCTF

- Luego intente leer y ejecutar el py entonces mejor vi el historial de la rama branch  y ya fui viendo lo que tenian las ramas que salian ,junte los resultados y pude sacar la bandera
`──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-2
cat flag.py
Switched to branch 'feature/part-2'
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-3
cat flag.py
Switched to branch 'feature/part-3'
print("Printing the flag...")

print("w0rk_7ae8dd33}")
`
[picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ae8dd33}]
