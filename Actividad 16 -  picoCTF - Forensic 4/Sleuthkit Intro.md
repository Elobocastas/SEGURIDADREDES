### 🚩 [## Sleuthkit Intro]

**Descripción:** Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz)

**Solucion**
- Aqui descargue el archivo y lo descomprimi para luego revisar todas las particiones
`(kali㉿kali)-[~/Downloads]
└─$ gunzip disk.img.gz
    ┌──(kali㉿kali)-[~/Downloads]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

- Luego entre al server para poner la patrticion y que me de el resultado 

┌──(kali㉿kali)-[~/Downloads]
└─$  nc chatelaine.cylabacademy.net 20589

What is the size of the Linux partition in the given disk image?
Length in sectors: 202752                         
202752
Great work!
academy{mm15_f7w!}





[ademy{mm15_f7w!}]
]
