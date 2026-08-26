**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Fix the syntax error in this Python script to print the flag.

**Solución:** Abri el archivo python y vi que no jalaba por la identacion y se la acomode al print  


codigo python 
`import random

def str_xor(secret, key):
    # Función interna que descifra la bandera
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for secret_c, new_key_c in zip(secret, new_key)])

flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x06) + chr(0x1c) + chr(0x5a) + chr(0x5c) + chr(0x55) + chr(0x40) + chr(0x3a) + chr(0x5f) + chr(0x53) + chr(0x5b) + chr(0x57) + chr(0x41) + chr(0x57) + chr(0x51) + chr(0x42) + chr(0x5d) + chr(0x42) + chr(0x5d) + chr(0x14)

flag = str_xor(flag_enc, 'bond')
print('That is correct! Here is your flag: ' + flag)

`


`┌──(kali㉿kali)-[~/Downloads]
└─$ nano fixme1.py 
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}

`



[picoCTF{1nd3nt1ty_cr1515_182342f7}]