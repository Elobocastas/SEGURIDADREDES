### 🚩 [PW Crackl 2 ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py)

and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

**Solución:**  Aqui descargue ambos archivos  y primero utilice un cat para leer el archivo de texto 
`┌──(kali㉿kali)-[~/Downloads]
└─$ cat level2.flag.txt.enc 

TY'1qM
      :
X:]RW]J                  

`
- Pero como me da cosas sin sentido voy a oasarme al otro archivo por ahora ,luego intente ejecutar el archivo py perop me pide contraseña

┌──(kali㉿kali)-[~/Downloads]
└─$ python level2.py level2.py 
Please enter correct password for flag: sas
That password is incorrect

Aqui lutilkice el cat para buscar igual el userpw para ver si me dice la contraseña 

`
┌──(kali㉿kali)-[~/Downloads]
└─$ cat level2.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()

`

- Aqui vi que me pone la contraseña en bin y voy a usar el python para traducirlo ç

`┌──(kali㉿kali)-[~/Downloads]
└─$ python           
Python 3.13.12 (main, Feb  4 2026, 15:06:39) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
`

- Puse lo que me arrojo y ya me dio la llave  \


`┌──(kali㉿kali)-[~/Downloads]
└─$ python3 level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
`

