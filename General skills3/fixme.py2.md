**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Fix the syntax error in the Python script to print the flag

**Solución:** Primero lo ejecute para ver que me arrogaba 

codigo python 

┌──(kali㉿kali)-[~/Downloads]
└─$ python3 fixme2.py 
  File "/home/kali/Downloads/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?



 - Luego utilice el nano para ver que tenia adentro Y  JUSTO TENIA un error de sintaxis donde nomas tiene un (=) en un if y esos llevan doble == entonces solo le puse el que faltaba 
import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x58) + chr(0x18) + chr(0x11) + chr(0x41) + chr(0x09) + chr(0x5f) + chr(0x1f) + chr(0x10) + chr(0x3b) + chr(0x1b) + chr(0x55)>

  
flag = str_xor(flag_enc, 'enkidu')

if flag == "":
  print('String XOR encountered a problem, quitting.' ) 
else:
  print('That is correct! Here\'s your flag: ' + flag)



`
Despues ya lo ejecute 
`
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}



`


[picoCTF{1nd3nt1ty_cr1515_182342f7}]