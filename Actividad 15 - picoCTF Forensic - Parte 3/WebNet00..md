### 🚩 [WEBNET00]

**Descripción:** We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.
**Solucion**
	Aqui utilice una extension que instale para p0oder leer los archivos e identtificar la bandera 
`──(kali㉿kali)-[~/Downloads]
└─$ ssldump -r webnet0-capture.pcap -k picopico.key -d | grep -A 3 academy
    61 67 3a 20 61 63 61 64 65 6d 79 7b 6e 6f 6e 67    ag: academy{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
    65 6e 67 74 68 3a 20 38 32 31 0d 0a 4b 65 65 70    ength: 821..Keep
Cleaned 3 remaining connection(s) from connection pool
--
    67 3a 20 61 63 61 64 65 6d 79 7b 6e 6f 6e 67 73    g: academy{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le
    6e 67 74 68 3a 20 31 30 30 0d 0a 4b 65 65 70 2d    ngth: 100..Keep-
┌──(kali㉿kali)-[~/Downloads]
`

`

[academy{nongsacademy{nongs
ers}
]
