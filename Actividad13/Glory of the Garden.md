### 🚩 [Glory of the garden]

**Descripción:** This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg)+codigo con el control + U  para poder ver que habia y ahi encontre la bandera  


**Solucion **
No pues solo descargue el archivo y utilice el comando para ver que tenia dentro la imagen  con un strings y filtre el ombre de acadamey para poder sacar la bandera 


`┌──(kali㉿kali)-[~/Downloads]
└─$ strings pico_img.png pico_img.png |grep academy
academy{s0_m3ta_b52e28f5}
academy{s0_m3ta_b52e28f5}

`
[academy{s0_m3ta_b52e28f5}
}