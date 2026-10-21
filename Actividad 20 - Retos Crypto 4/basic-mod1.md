### 🚩 [- basic-mod1]

**Descripción:**We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://challenge-files.cylabacademy.net/library/f3895827512c6fab64095a69942e62ba9e367bb32d70ff69dc0e8fd9a826936a/message.txt)

.

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`
*Solucion* 
No pues aqui hice un script igual para la imagen este es 
`# Mapeo de caracteres según las instrucciones del reto
def decodificar_numero(num):
    val = num % 37
    if 0 <= val <= 25:
        # 0-25 es el alfabeto en mayúsculas (ASCII de 'A' es 65)
        return chr(val + 65)
    elif 26 <= val <= 35:
        # 26-35 son los dígitos 0-9
        return str(val - 26)
    elif val == 36:
        # 36 es un guion bajo
        return "_"
    return ""

#Leer el archivo con los números
 Cambia 'message.txt' por el nombre real de tu archivo si es diferente
with open("message.txt", "r") as file:
    contenido = file.read()

Separar los números (asumiendo que están separados por espacios)
numeros = contenido.strip().split()

 Decodificar cada número y unir el texto
mensaje_decifrado = ""
for n in numeros:
    mensaje_decifrado += decodificar_numero(int(n))

Imprimir con el formato de bandera que pide CyLab Academy
print(f"academy{{{mensaje_decifrado}}}")`

┌──(kali㉿kali)-[~/Downloads]
└─$ python3  solve_mod1.py 
academy{R0UND_N_R0UND_65371195}


`
 Ya solo lo ejecute y venia la respuesta 
[academy{R0UND_N_R0UND_65371195}
}
