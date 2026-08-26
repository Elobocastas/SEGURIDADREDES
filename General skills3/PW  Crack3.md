### 🚩 [PW Crackl 23]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py)

and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

**Solución:**  Aqui descargue todos los archivos y despues utilice cat para buscar la contraseña en el archivo .py y me salio esto 

`┌──(kali㉿kali)-[~/Downloads]
└─$ cat level3.py 
import hashlib

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

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

`


- Solo tuve que probar entre esas 7 combinaciones para resolverlo 

`┌──(kali㉿kali)-[~/Downloads]
└─$ python3 level3.py 
Please enter correct password for flag: f09e
That password is incorrect
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
┌──(kali㉿kali)-[~/Downloads]
└─$                 
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 level3.py  
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
`
