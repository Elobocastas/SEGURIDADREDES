### 🚩 [- - - MacroHard WeakEdge]

**Descripción:** I've hidden a flag in this file. Can you find it? [Forensics_is_fun.pptm](https://challenge-files.cylabacademy.net/library/ef35dfe613527d28fe872d94179b53bc1a0497ddecf57e51d160c910be3a8e8a/Forensics_is_fun.pptm) 
**Solucion**
Para resolver **Forensics_is_fun.pptm**, tratamos la presentación como un archivo ZIP y extrajimos su estructura interna desde la terminal. Tras descartar una macro falsa que servía como señuelo, localizamos un archivo sospechoso sin extensión llamado `hidden` dentro de la carpeta `slideMasters`. Descubrimos que la bandera estaba ofuscada con espacios y codificada en Base64, por lo que utilizamos una tubería de comandos (`cat`, `tr -d ' '` y `base64 -d`) para limpiar los espacios, decodificar el texto y revelar la bandera final.

`┌──(kali㉿kali)-[~/Downloads]
└─$ cat reto_pptm/ppt/slideMasters/hidden | tr -d ' ' | base64 -d
flag: academy{D1d_u_kn0w_ppts_r_z1p5}    `
[academy{D1d_u_kn0w_ppts_r_z1p5}   

]
