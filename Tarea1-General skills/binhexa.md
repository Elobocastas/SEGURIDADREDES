### 🚩 [- binhexa]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
How well can you perfom basic binary operations?

**Solución:** No pues aqui me conecte para ver que me pedia y eran varias preguntas y utilice el python que tiene la consola para resolver lo que me iba pidiendo '
`┌──(kali㉿kali)-[~]
└─$ python           
Python 3.13.12 (main, Feb  4 2026, 15:06:39) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(0b10011011 & 0b10111100)
'0b10011000'
>>> bin(0b10011011 << 1)
'0b100110110'
>>> bin(0b10011011 | 0b10111100)
'0b10111111'
>>> bin(0b10111100 >> 1)
'0b1011110'
>>> bin(0b10011011 + 0b10111100)
'0b101010111'
>>> bin(0b10011011 * 0b10111100)
'0b111000111010100'
>>> hex(0b111000111010100)
'0x71d4'
>>>     
'


- Y esto era lo que iba respondiendo hasta llegar a la bandera 
`┌──(kali㉿kali)-[~]
└─$ nc titan.picoctf.net 56000        

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10011011
Binary Number 2: 10111100


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b10011000 
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 0b100110110
Correct!

Question 3/6:
Operation 3: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b10111111
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 0b1011110
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b101010111
Correct!

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b111000111010100
Correct!

Enter the results of the last operation in hexadecimal: 0x71d4

Correct answer!
The flag is: [picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
`