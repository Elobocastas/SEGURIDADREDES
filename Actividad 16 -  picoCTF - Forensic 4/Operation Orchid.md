### 🚩 [- Operation Orchid]

**Descripción:** Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/7d645367284f9df9139dd5ad212e5c3bd0815b7674ca700648a3983158394892/disk.flag.img.gz) 
**Solucion**
ara resolver **Operation Orchid**, la onda fue básicamente explorar el disco y husmear en el historial de comandos del atacante (el archivo `.ash_history`). Ahí vimos que el tipo había encriptado la bandera, pero cometió el error de dejar la contraseña anotada en el historial (`unbreakablepassword1234567`).

Luego, solo usamos `icat` para sacar el archivo encriptado de las entrañas del disco y ejecutamos `openssl` para quitarle el candado. El único detallito fue ajustarle el algoritmo (`-md sha256`) para que nuestro Kali nuevo se entendiera con el cifrado viejo, ¡y pum, bandera recuperada!


`┌──(kali㉿kali)-[~/Downloads]
└─$ openssl aes-256-cbc -d -salt -in flag.txt.enc -out bandera_final.txt -k unbreakablepassword1234567 -md sha256
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
400705CB587F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107
┌──(kali㉿kali)-[~/Downloads]
└─$ cat bandera_final.txt
academy{h4un71ng_p457_718ebd29}         `
[academy{h4un71ng_p457_718ebd29} }]
]
