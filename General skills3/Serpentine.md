### 🚩 [- Serpentine ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Find the flag in the Python script!

**Solución:**  Aqui lo que hice fue ejecutar y ver qu4e podia hacer ,probe las opciones pero nimguna me daba el resultado que queria 

`

└─$ python3 serpentine.py 
/home/kali/Downloads/serpentine.py:41: SyntaxWarning: invalid escape sequence '\ '
  /     \      .- ~ ~ -.

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
Keep it up!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

`



- Entonces utilice nano para pode ver el codigo de mejor manera

y vi que no estaba la funcion en el elif d (b) y solo la rremplace por la que deberia de estar
`elif choice == 'b':
    print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')`


- Remplace a 

`elif choice == 'b':
    print_flag()
    
    `

- Solo ejecute y ya  
`┌──(kali㉿kali)-[~/Downloads]
└─$ python3 serpentine.py 
/home/kali/Downloads/serpentine.py:41: SyntaxWarning: invalid escape sequence '\ '
  /     \      .- ~ ~ -.

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) B

I did not understand "B", input only "a", "b" or "c"


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) 
`



[picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}]