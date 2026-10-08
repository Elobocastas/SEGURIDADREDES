### 🚩 [Milkslap]

**Descripción:** We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.
**Solucion**
Primero desargue la imagen para buscar cosas dentro de ella 
luego extraje los datos con  zteg 
`wget http://xebec.cylabacademy.net:46577/concat_v.png
--2026-10-07 12:32:47--  http://xebec.cylabacademy.net:46577/concat_v.png
Resolving xebec.cylabacademy.net (xebec.cylabacademy.net)... 3.14.181.178
Connecting to xebec.cylabacademy.net (xebec.cylabacademy.net)|3.14.181.178|:46577... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095896 (17M) [image/png]
Saving to: ‘concat_v.png’
- Luego ya busque la bandera con otro comando y ya
`┌──(kali㉿kali)-[~]
└─$ RUBY_THREAD_VM_STACK_SIZE=500000000 zsteg concat_v.png | grep -iE "academy|picoCTF"

b1,b,lsb,xy         .. text: "academy{imag3_m4n1pul4t10n_sl4p5}\n"
`


[academy{imag3_m4n1pul4t10n_sl4p5}]
]
