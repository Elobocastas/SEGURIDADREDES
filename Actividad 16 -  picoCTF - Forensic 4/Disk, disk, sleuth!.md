### 🚩 []

**Descripción:** Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/4d6e776c4f09366b282fa45c00b74c0e348309a34f636fd6a9e4e0ee50e7345b/dds1-alpine.flag.img.gz) 
**Solucion**
- Aqui lo que hice fue Instalar una herramienta para ver una imagen comprimida
Instalar The Sleuth Kit
- lo voy a extraer y buscar lo que quiero con un comando especifico que es r `srch_strings` 
`┌──(kali㉿kali)-[~/Downloads]
└─$ zcat dds1-alpine.flag.img.gz | srch_strings | grep -iE "academy|picoCTF"
  SAY academy{f0r3ns1c4t0r_n30phyt3_6502313d}
`

[academy{f0r3ns1c4t0r_n30phyt3_6502313d]
]
