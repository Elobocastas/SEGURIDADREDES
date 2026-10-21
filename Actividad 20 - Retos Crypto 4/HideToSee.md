### 🚩 [- HideToSee]

**Descripción:**How about some hide and seek heh? Look at this image [here](https://challenge-files.cylabacademy.net/library/4430e164c62a6474394efb666c3b2c24511a0823a3408e5e7a19a37940f0e592/atbash.jpg).

.

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`
*Solucion* 
No pues aqui extraje la imagen y luego cree un scprit en python para poder leerlo 
`┌──(kali㉿kali)-[~/Downloads]
└─$ steghide extract -sf atbash.jpg
`
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 sasasa.py 
academy{atbash_crack_6167bd8e}
`import string # Cambia "encrypted.txt" si el archivo extraído se llama diferente with open("encrypted.txt", "r") as f: texto_cifrado = f.read().strip() # Preparar los abecedarios normales e invertidos abc_min = string.ascii_lowercase abc_may = string.ascii_uppercase atbash_min = abc_min[::-1] # Abecedario al revés atbash_may = abc_may[::-1] # Crear una tabla de traducción y aplicarla tabla = str.maketrans(abc_min + abc_may, atbash_min + atbash_may) texto_descifrado = texto_cifrado.translate(tabla) print(texto_descifrado)`


[academy{atbash_crack_6167bd8e}
]
