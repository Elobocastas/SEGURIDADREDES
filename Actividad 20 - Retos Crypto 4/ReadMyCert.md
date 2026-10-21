### 🚩 [- ReadMyCert]

**Descripción:**How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://challenge-files.cylabacademy.net/library/936e82e74aef68c1a8fcc80b032ea33d65adda1f04b5c46085d44a5d6ff7cb71/readmycert.csr).
*Solucion*
No pues aqui simplemente abri elo archivo y busque un poco ahi la bandera 
`┌──(kali㉿kali)-[~/Downloads]
└─$ openssl req -in readmycert.csr -noout -text
Certificate Request:
    Data:
        Version: 1 (0x0)
        Subject: CN=academy{read_mycert_dcfb9c76}, name=ctfPlayer
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (2048 bit)
                Modulus:
`



[academy{read_mycert_dcfb9c76}
]
