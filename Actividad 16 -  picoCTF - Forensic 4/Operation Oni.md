### 🚩 [- Operation Oni]

**Descripción:** Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.


**Solucion**
Para resolver **Operation Oni**, el objetivo era infiltrarnos en un servidor usando una llave SSH escondida en el disco. Usamos `fls` para localizar la llave privada (`id_ed25519`) y la extrajimos con `icat` usando su inodo (2345). Después, le aplicamos los permisos de seguridad obligatorios con `chmod 600` para que la conexión no nos rebotara. Con la llave lista, nos conectamos por SSH al servidor remoto, entramos directo y sacamos la bandera leyendo el archivo `flag.txt`.


`┌──(kali㉿kali)-[~/Downloads]
└─$ icat -o 206848 disk.img 2345 > mi_llave_ssh

┌──(kali㉿kali)-[~/Downloads]
└─$ chmod 600 mi_llave_ssh
┌──(kali㉿kali)-[~/Downloads]
└─$ ssh -i mi_llave_ssh -p 31251 ctf-player@xebec.cylabacademy.net
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 7.0.0-1014-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat 
.cache/   .ssh/     flag.txt  
ctf-player@challenge:~$ cat 
.cache/   .ssh/     flag.txt  
ctf-player@challenge:~$ cat flag.txt
academy{k3y_5l3u7h_f52dbc2c}ctf-player@challenge:~$ Connection to xebec.cylabacademy.net closed by remote host.
Connection to xebec.cylabacademy.net closed.
`
[academy{k3y_5l3u7h_f52dbc2c}}]
]
