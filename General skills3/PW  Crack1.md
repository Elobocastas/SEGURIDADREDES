### 🚩 [PW Crackl  ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py)

and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

	**Solución:**  Aqui solo tuve que descargar los archivos y utilice uun cat para ver el contenido de level1 yA QUE me pide contraseña y ahi vi cual era 
`─$ cat level1.py 
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


flag_enc = open('level1.flag.txt.enc', 'rb').read()
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
level_1_pw_check()

`
ahi en user_pw dice y nomas es de ejhecutarlo ,la puse y me lanzo el resultado 



└─$ python level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
[picoCTF{545h_r1ng1ng_56891419}
