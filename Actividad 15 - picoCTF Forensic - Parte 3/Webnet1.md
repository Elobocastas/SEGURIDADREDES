### 🚩 [- Webnet1]

**Descripción:** We found this [packet capture](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key). Recover the flag.
**Solucion**ç
No pues aqui descargue los archivos y yas utilice igual ciertos comandos para entrar a los arfhivo9s y filtrar la bandera utilizando las funcionalidades del shark 
`┌──(kali㉿kali)-[~/Downloads/archivos_webnet1]
└─$ ssldump -r webnet1-capture.pcap -k "picopico(1).key" -d | grep -A 5 academy
    61 67 3a 20 61 63 61 64 65 6d 79 7b 74 68 69 73    ag: academy{this
    2e 69 73 2e 6e 6f 74 2e 79 6f 75 72 2e 66 6c 61    .is.not.your.fla
    67 2e 61 6e 79 6d 6f 72 65 7d 0d 0a 43 6f 6e 74    g.anymore}..Cont
    65 6e 74 2d 4c 65 6e 67 74 68 3a 20 38 34 37 0d    ent-Length: 847.
    0a 4b 65 65 70 2d 41 6c 69 76 65 3a 20 74 69 6d    .Keep-Alive: tim
    65 6f 75 74 3d 35 2c 20 6d 61 78 3d 31 30 30 0d    eout=5, max=100.
--
    67 3a 20 61 63 61 64 65 6d 79 7b 74 68 69 73 2e    g: academy{this.
    69 73 2e 6e 6f 74 2e 79 6f 75 72 2e 66 6c 61 67    is.not.your.flag
    2e 61 6e 79 6d 6f 72 65 7d 0d 0a 43 6f 6e 74 65    .anymore}..Conte
    6e 74 2d 4c 65 6e 67 74 68 3a 20 31 30 30 0d 0a    nt-Length: 100..
    4b 65 65 70 2d 41 6c 69 76 65 3a 20 74 69 6d 65    Keep-Alive: time
    6f 75 74 3d 35 2c 20 6d 61 78 3d 31 30 30 0d 0a    out=5, max=100..
--
    Pico-Flag: academy{this.is.not.your.flag.anymore}
    Keep-Alive: timeout=5, max=99
    Connection: Keep-Alive
    Content-Type: image/jpeg
    
    ---------------------------------------------------------------
--
    00 00 00 01 00 00 00 01 61 63 61 64 65 6d 79 7b    ........academy{
    68 6f 6e 65 79 2e 72 6f 61 73 74 65 64 2e 70 65    honey.roasted.pe
    61 6e 75 74 73 7d 00 00 ff e2 02 1c 49 43 43 5f    anuts}......ICC_
    50 52 4f 46 49 4c 45 00 01 01 00 00 02 0c 6c 63    PROFILE.......lc
    6d 73 02 10 00 00 6d 6e 74 72 52 47 42 20 58 59    ms....mntrRGB XY
    5a 20 07 dc 00 01 00 19 00 03 00 29 00 39 61 63    Z .........).9ac
Cleaned 4 remaining connection(s) from connection pool
`
	
[academy{honey.roasted.peanuts}

]
