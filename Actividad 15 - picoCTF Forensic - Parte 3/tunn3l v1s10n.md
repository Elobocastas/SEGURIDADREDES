### 🚩 [- - tunn3l v1s10n]

**Descripción:** We found this file. Recover the flag. [tunn3l_v1s10n](https://challenge-files.cylabacademy.net/library/3b5add918cb4cf98fa62ef4e05eb8c55c6c9ae547a939c6be992ee3aa656ee69/tunn3l_v1s10n)
**Solucion**
No pues como esta encriptada la respuesta yo utilice un script en python para poder resolverlo y ester fue 
`# solve.py
with open("tunn3l_v1s10n", "rb") as f:
    data = bytearray(f.read())

# 1. Reparar el offset de los píxeles (posición 0x0A). 
# El estándar de BMP es 54 bytes (0x36 en hexadecimal)
data[10:14] = b'\x36\x00\x00\x00'

# 2. Reparar el tamaño de la cabecera DIB (posición 0x0E). 
# El estándar es 40 bytes (0x28 en hexadecimal)
data[14:18] = b'\x28\x00\x00\x00'

# 3. La trampa del "Tunnel Vision" (Visión de túnel):
# Si solo reparas lo de arriba, verás una imagen recortada con una bandera falsa "notaflag{}".
# Necesitamos aumentar la altura de la imagen (posición 0x16) para revelar la parte oculta.
# Cambiamos la altura a unos 850 píxeles (0x0352 en hexadecimal, little-endian)
data[22:26] = b'\x52\x03\x00\x00'

# Guardar la imagen reparada
with open("bandera_revelada.bmp", "wb") as f:
    f.write(data)
    
print("¡Archivo reparado! Abre bandera_revelada.bmp")



└─$ python3 solve.py 
¡Archivo reparado! Abre bandera_revelada.bmp
┌──(kali㉿kali)-[~/Downloads]
└─$ open bandera_revelada.bmp 
`

academy{qu1t3_a_v13w_2020}

]
