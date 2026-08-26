### 🚩 [convertme  ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Run the Python script and convert the given number from decimal to binary to get the flag

**Solución:** Aqui hice un pequeño programa en python para poder traducir el numero a bin y simplemente ejecute 

*** Codigo 1

──(kali㉿kali)-[~/Downloads]
└─$ python
Python 3.13.12 (main, Feb  4 2026, 15:06:39) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> # Guardamos el número en una variable 
... numero_decimal = 90
... 
... # Convertimos a binario usando la función bin()
... resultado_binario = bin(numero_decimal)[2:]
... 
... #  resultado 
... print(f"El número {numero_decimal} en binario es: {resultado_binario}")
... 
El número 90 en binario es: 1011010
`

`
codigo 2
`┌──(kali㉿kali)-[~/Downloads]
└─$ python3 convertme.py 
If 90 is in decimal base, what is it in binary base?
Answer: 1011010
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
`





[picoCTF{4ll_y0ur_b4535_9c3b7d4d}


**Referencias :
https://docs.python.org/es/3/library/functions.html#bin
