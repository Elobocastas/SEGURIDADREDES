### 🚩 [Super SSH ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Using a Secure Shell (SSH) is going to be pretty important.

**Solución:**  No pues aqui mi solucion fue simple utilice a ssh para conectarme utilizando el ssh  con la direccion que habia y solo puse la contraseña que ahi decia 

 `┌──(kali㉿kali)-[~]
└─$  ssh ctf-player@titan.picoctf.net  -p 49726 

`The authenticity of host '[titan.picoctf.net]:49726 ([3.139.174.234]:49726)' can't be established.
ED25519 key fingerprint is: SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:49726' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_5d09a462}
Connection to titan.picoctf.net closed.`


[picoCTF{s3cur3_c0nn3ct10n_5d09a462}]



