### 🚩 [- Scavenger Hunt]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?

There is some interesting information hidden around this site. Can you find it?
*Solucion* 
Aqui entre a la pagina y me puse a ver el codigo  luego el css y ya me puse a probar en la consola para resolver las otras partes de la bandera 

`┌──(kali㉿kali)-[~/Downloads]
└─$ curl -s http://wily-courier.picoctf.net:60148/robots.txt
User-agent: *
Disallow: /index.html
Part 3: t_0f_pl4c
 I think this is an apache server... can you Access the next flag?

┌──(kali㉿kali)-[~/Downloads]
└─$ 
    
┌──(kali㉿kali)-[~/Downloads]
└─$ curl -s http://wily-courier.picoctf.net:60148/.htaccess
Part 4: 3s_2_lO0k
┌──(kali㉿kali)-[~/Downloads]
└─$ curl -s http://wily-courier.picoctf.net:60148/.DS_Store
Congrats! You've completed the scavenger hunt! Part 5: _9588550}
`


[picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}}
