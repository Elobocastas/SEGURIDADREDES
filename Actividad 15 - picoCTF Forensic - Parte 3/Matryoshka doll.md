### 🚩 [- Matryoshka doll]

**Descripción:** Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.cylabacademy.net/library/a268db7b2edb5615a738f69c2c79faa4d8a6bcde6b0f2f797a8f319cb52fe2a5/dolls.jpg)
**Solucion**
Aqui utlice el binwalk pasra poder desincriptar los archivos tons fue nomas poner unos comandos y ya poder ver la informacion oculta
`┌──(kali㉿kali)-[~/Downloads]
└─$ grep -r "academy" .
grep: ./_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/4_c.jpg: binary file matches
./_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/flag.txt:academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
grep: ./_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/136DA.zip: binary file matches
grep: ./_dolls.jpg-1.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/4_c.jpg: binary file matches
./_dolls.jpg-1.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/flag.txt:academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
grep: ./_dolls.jpg-1.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/136DA.zip: binary file matches
grep: ./pico_img.png: binary file matches
grep: ./_dolls.jpg-0.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/4_c.jpg: binary file matches
./_dolls.jpg-0.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/flag.txt:academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
grep: ./_dolls.jpg-0.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted/136DA.zip: binary file matches
`


[academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}}

]
