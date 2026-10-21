### 🚩 [Pixelated]

**Descripción:** I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.cylabacademy.net/library/198460e9f994fd1edb510f1950a00809b457cc8ce4ce3ccd70fb3efad87343d4/scrambled1.png) [scrambled2.png](https://challenge-files.cylabacademy.net/library/198460e9f994fd1edb510f1950a00809b457cc8ce4ce3ccd70fb3efad87343d4/scrambled2.png)
*Solucion* 
No pues yo hice un script de python para poder atacar esas dos imagenes tons 
`import numpy as np from PIL import Image # Cargar las imágenes y convertirlas a enteros más grandes img1 = np.array(Image.open("scrambled1.png")).astype(int) img2 = np.array(Image.open("scrambled2.png")).astype(int) # Realizar la suma y el módulo sin problemas de desbordamiento resultado = (img1 + img2) % 256 # Volver a convertir a uint8 para poder guardarlo como imagen imagen_final = Image.fromarray(resultado.astype('uint8')) imagen_final.save("flag.png")`
`
 Ya solo lo ejecute y abri la imagen y venia la respuesta 
[academy{2f16d0c4}}
