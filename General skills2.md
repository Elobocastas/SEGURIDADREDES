# CyberLab - General Skills 2

## 🚩 Based

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

**Solución:** `picoCTF{learning_about_converting_values_acdCcfCa}`

**Código 1:**

Bash

```
┌──(kali㉿kali)-[~]
└─$ python
Python 3.13.12 (main, Feb  4 2026, 15:06:39) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
"".join([chr(int(c, 2)) for c in "01110000 01101001 01100101".split()])
'pie'
"".join([chr(int(c.replace('o', ''), 8)) for c in "o143 o157 o156 o164 o141 o151 o156 o145 o162".split()])
'container'
bytes.fromhex("616e696d6174696f6e").decode("utf-8")
'animation'
```

**Código 2:**

Bash

```
┌──(kali㉿kali)-[~] └─$ nc fickle-tempest.picoctf.net 63213  Let us see how data is stored test Please give the 01110100 01100101 01110011 01110100 as a word. ... you have 45 seconds.....`
Input:
test
Please give me the  o163 o157 o143 o153 o145 o164 as a word.
Input:
Too slow!
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 63213
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....
Input:
falcon
Please give me the  o141 o156 o151 o155 o141 o164 o151 o157 o156 as a word.
Input:
Too slow!
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 63213 
Let us see how data is stored
lamp
Please give the 01101100 01100001 01101101 01110000 as a word.
...
you have 45 seconds.....
Input:
lamp
Please give me the  o163 o165 o142 o155 o141 o162 o151 o156 o145 as a word.
Input:
Too slow!
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 63213 
Let us see how data is stored
light
Please give the 01101100 01101001 01100111 01101000 01110100 as a word.
...
you have 45 seconds.....
Input:
Too slow!
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 63213 
Let us see how data is stored
lizard
Please give the 01101100 01101001 01111010 01100001 01110010 01100100 as a word.
...
you have 45 seconds.....
Input:
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net49402
fickle-tempest.picoctf.net49402: forward host lookup failed: Unknown host
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 49402
Let us see how data is stored
pie
Please give the 01110000 01101001 01100101 as a word.
...
you have 45 seconds.....
Input:
pie
Please give me the  o143 o157 o156 o164 o141 o151 o156 o145 o162 as a word.
Input:
container
Please give me the 616e696d6174696f6e as a word.
Input:
animation
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}
```

> [!bug] Anotación de Errores en Terminal
> 
> - **Error de sintaxis en `nc`:** Falta de espacio entre el dominio y el puerto (`fickle-tempest.picoctf.net49402`), lo que provoca que el comando falle con el error `forward host lookup failed: Unknown host`.
>     
> - **Tiempo agotado:** Respuesta demasiado lenta (`Too slow!`). Es necesario agilizar la conversión e ingreso de los datos requeridos por el servidor.
>     

**Notas adicionales:** Ser rapido con las terminales **Referencias:**

## 🚩 strings it

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Can you find the flag in file without running it?

**Solución:** `picoCTF{5tRIng5_1T_FB7D7Bb6}`

**Código:**

Plaintext

```
┌──(kali㉿kali)-[~]
└─$ DIR
DIR: command not found
┌──(kali㉿kali)-[~]
└─$ dir
Desktop  Documents  Downloads  Music  Pictures  Projects  Public  Templates  Videos
┌──(kali㉿kali)-[~]
└─$ cdd Downloads
Command 'cdd' not found, but there are 17 similar ones.
┌──(kali㉿kali)-[~]
└─$ cd Downloads 
┌──(kali㉿kali)-[~/Downloads]
└─$ dir
file  flag  strings
┌──(kali㉿kali)-[~/Downloads]
└─$ cat strings
ELF>@h
@@@@▒▒▒pp55   -==t))-==888 XXXDDStd888 PtdH H H DDQtdRtd-==PP/lib64/ld-linux-x86-64.so.2GNUGNUue_O1D7GNUem)L
&.[ w "▒(libc.so.6putsstdoutcxa_finalizesetvbuflibc_start_mainGLIBC_2.2.5gmonstartITH=2/H=qVHjVH9tH/HtregH=AVH5:VH)HH?HHHtH.HfD=Vu+UH=.Ht%/hh%/D%]/D%U/D1I^HHPTLH
H=.  dU]wUHH}HuHUHH=gAWL=+AVIAUIATAUH-+SL)HHt1LLDAHH9uH[]A\A]A^Aff.HHMaybe try the 'strings' function? Take a look at the man pageD▒8!h8zRx                                                                                                                              /D$4X0F▒J {                                                                                                                                            ?▒:*3$"\tX IDEC
... [Output Binario Omitido] ...
┌──(kali㉿kali)-[~/Downloads]
└─$ 1;2c1;2c1;2c strings strings | grep "picoCTF"
1: command not found
2c1: command not found
2c1: command not found
2c: command not found
┌──(kali㉿kali)-[~/Downloads]
└─$ strings strings | grep "picoCTF"
picoCTF{5tRIng5_1T_FB7D7Bb6}
```

> [!bug] Anotación de Errores en Terminal
> 
> - **Sensibilidad a mayúsculas:** Uso de mayúsculas en comandos (`DIR` en lugar de `dir` o `ls`). En entornos Linux, esto devuelve `command not found`.
>     
> - **Error tipográfico en comandos:** Ingreso de `cdd` con doble "d" al intentar navegar entre directorios.
>     
> - **Basura en la entrada estándar:** Presencia de caracteres residuales en el prompt (`1;2c1;2c1;2c strings...`), ocasionados comúnmente por secuencias de escape ANSI mal interpretadas o clics accidentales en la terminal.
>     

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 Wave a flag

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

**Solución:** Plaintext

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 Static ain't always noise

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Can you look at the data in this binary? The bash script might help!

**Solución:** `picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}`

**Código:**

Bash

```
┌──(kali㉿kali)-[~/Downloads]
└─$ dir
file  flag  strings  warm
┌──(kali㉿kali)-[~/Downloads]
└─$ cat warm
@#@@@▒▒▒pp   88-==hp-==888 XXXDDStd888 Ptd   DDQtdRtd-==XX/lib64/ld-linux-x86-64.so.2GNUGNUF)KgGNemK 
                                                                                                                                           -&g v "libc.so.6putsprintf__cxa_finalizestrcmp__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMClone?H=/H=9/H2/H9tH.HterH=ableu▒i /H5/H)HH?HHHtH.HfD=.u+UH=.Hthh%/D%E/D%=/D%5/D1I^HHPTLH
                                                                                                       H=.d.]wUHH}Hu}uH=_KHEHHH5wHuH=kHEHHHH=fAWL=+AVIAUIATAUH-+SL)HHt1LLDAHH9uH[]A\A]A^A_ff.HHHello user! Pass me a -h to learn what I can do!-hOh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}I don't know what '%s' means! I do know what -h means though!
D8xx`▒8zRx
... [Output Binario Omitido] ...
┌──(kali㉿kali)-[~/Downloads]
└─$ chmod +x warm
./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 useless

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? There's an interesting script in the user's home directory

**Solución:** `picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5136}`

**Código:**

Bash

```
┌──(kali㉿kali)-[~]
└─$ ssh  saturn.picoctf.net Port: 57715
The authenticity of host 'saturn.picoctf.net (13.59.203.175)' can't be established.
ED25519 key fingerprint is: SHA256:UC2PVUPRjF0owqLaO35EY6awgmeLuxkIuYc1C9abJH0
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'saturn.picoctf.net' (ED25519) to the list of known hosts.
kali@saturn.picoctf.net: Permission denied (publickey).
┌──(kali㉿kali)-[~]
└─$ ssh picoplayer@saturn.picoctf.net -p 57715
The authenticity of host '[saturn.picoctf.net]:57715 ([13.59.203.175]:57715)' can't be established.
ED25519 key fingerprint is: SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? password
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[saturn.picoctf.net]:57715' (ED25519) to the list of known hosts.
WARNING: connection is not using a post-quantum key exchange algorithm.
 This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
picoplayer@saturn.picoctf.net's password:
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.17.0-1019-aws x86_64)
Documentation:  https://help.ubuntu.com
Management:     https://landscape.canonical.com
Support:        https://ubuntu.com/advantage
The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.
Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.
picoplayer@challenge:~$ man useless
useless
useless, — This is a simple calculator script
SYNOPSIS
useless, [add sub mul div] number1 number2
DESCRIPTION
Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.
Examples
./useless add 1 2
This will add 1 and 2 and return 3
 ./useless mul 2 3
   This will return 6 as a product of 2 and 3
 ./useless div 6 3
   This will return 2 as a quotient of 6 and 3
 ./useless sub 6 5
   This will return 1 as a remainder of substraction of 5 from 6
Authors
This script was designed and developed by Cylab Africa
 picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5136}
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```

> [!bug] Anotación de Errores en Terminal
> 
> - **Conexión SSH denegada y sintaxis de puerto:** Intento de conexión omitiendo el usuario del reto (lo que fuerza el uso del usuario local `kali`) y empleando una sintaxis no válida para designar el puerto (`Port: 57715` en lugar de `-p 57715`). El resultado es el error `Permission denied (publickey)`.
>     

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 Tab, Tab, Attack

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.

**Solución:** `picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}`

**Código:**

Plaintext

```
┌──(kali㉿kali)-[~]
└─$ dir
Desktop  Documents  Downloads  Music  Pictures  Projects  Public  Templates  Videos
┌──(kali㉿kali)-[~]
└─$ cd Downloads
┌──(kali㉿kali)-[~/Downloads]
└─$ dir
Addadshashanammu.zip  file  flag  gemini-code-1787584453128.sh  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
┌──(kali㉿kali)-[~/Downloads]
└─$ cat Addadshashanammu.zip
PK
[Addadshashanammu/UT 3k<i4k<iux
PK
[ Addadshashanammu/Almurbalarammi/UT 3k<i4k<iux
PK
[/Addadshashanammu/Almurbalarammi/Ashalmimilkala/UT  3k<i4k<iux
PK
[?Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/UT  3k<i4k<iux
PK
[LAddadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/UT     3k<i4k<iux
PK
[YAddadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/UT        3k<i4k<iux
PK
[gAddadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/UT  4k<i4k<iux
PK
[d>%``~Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.cUT      3k<i4k<iux
#include <stdio.h>
int main(){
printf("ZAP! picoCTF{l3v3lup!_t4k3_4_r35t!_fc588427}\n");
}
P[2       HA|Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnametUT       4k<i4k<iux
... [Output Binario Omitido] ...
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
creating: Addadshashanammu/
creating: Addadshashanammu/Almurbalarammi/
creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c
inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
┌──(kali㉿kali)-[~/Downloads]
└─$ ./Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
ZAP! picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
┌──(kali㉿kali)-[~/Downloads]
└─$ 
```

> [!bug] Anotación de Errores en Terminal
> 
> - **Uso de `cat` en archivos empaquetados:** Intento de lectura directa de un archivo comprimido (`cat Addadshashanammu.zip`). Leer un `.zip` o archivo binario mediante este comando imprime contenido ilegible en la consola y corre el riesgo de desconfigurar la terminal. Se requiere la herramienta `unzip`.
>     

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 Magikarp Ground Mission

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Do you know how to move between directories and read files in the shell? Start the container, ssh to it, and then ls once connected to begin.

**Solución:** `picoCTF{xxsh0ut_0f//4t3r_0b24fc4f}`

**Código:**

Bash

```
┌──(kali㉿kali)-[~]
└─$ ssh ctf-player@ wily-courier.picoctf.net -p56753
ssh: Could not resolve hostname : Name or service not known
┌──(kali㉿kali)-[~]
└─$ ssh ctf-player@wily-courier.picoctf.net -p56753
WARNING: connection is not using a post-quantum key exchange algorithm.
 This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@wily-courier.picoctf.net's password:
Permission denied, please try again.
ctf-player@wily-courier.picoctf.net's password:
Permission denied, please try again.
ctf-player@wily-courier.picoctf.net's password:
ctf-player@wily-courier.picoctf.net: Permission denied (publickey,password).
┌──(kali㉿kali)-[~]
└─$ ssh ctf-player@wily-courier.picoctf.net -p56753
WARNING: connection is not using a post-quantum key exchange algorithm.
 This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@wily-courier.picoctf.net's password:
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 6.17.0-1013-aws x86_64)
Documentation:  https://help.ubuntu.com
Management:     https://landscape.canonical.com
Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.
To restore this content, you can run the 'unminimize' command.
The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.
Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.
ctf-player@pico-chall$ dir
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat
1of3.flag.txt             instructions-to-2of3.txt
ctf-player@pico-chall$ cat./instructions-to20f3.txt
-bash: cat./instructions-to20f3.txt: No such file or directory
ctf-player@pico-chall$ cat lof3.flag.txt
cat: lof3.flag.txt: No such file or directory
ctf-player@pico-chall$ cat lof3.flag
cat: lof3.flag: No such file or directory
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ dir
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat
.dockerenv                boot/                     etc/                      lib/                      mnt/                      root/                     srv/                      usr/
2of3.flag.txt             challenge/                home/                     lib64/                    opt/                      run/                      sys/                      var/
bin/                      dev/                      instructions-to-3of3.txt  media/                    proc/                     sbin/                     tmp/
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f//4t3r_
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ dir
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat instructions-to-3of3.txt
Lastly, ctf-player, go home... more succinctly ~
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ dir
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cT 3of3.flag.txt
-bash: cT: command not found
ctf-player@pico-chall$ cat 3of3.flag.txt
0b24fc4f}ctf-player@pico-chall$ Connection to wily-courier.picoctf.net closed by remote host.
Connection to wily-courier.picoctf.net closed.
```

> [!bug] Anotación de Errores en Terminal
> 
> - **Sintaxis en SSH:** Inserción de un espacio sobrante en `ctf-player@ wily-courier...`, lo cual impide la correcta resolución del hostname.
>     
> - **Espaciado en comandos:** Ejecución de `cat./instructions-to20f3.txt` sin el espacio reglamentario entre la instrucción y el argumento.
>     
> - **Errores tipográficos de nombres de archivo:** Sustitución de la letra 'o' por un cero (`20` en lugar de `2o`), y confusión visual entre la letra 'l' minúscula y el número '1' (`lof3` en vez de `1of3`).
>     
> - **Comando inválido:** Introducción del comando `cT` en lugar de `cat`, provocando el error `command not found`.
>     

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 repetitions

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Can you make sense of this file?

**Solución:** `picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}`

**Código:**

Bash

```
┌──(kali㉿kali)-[~]
└─$ dir
Desktop  Documents  Downloads  Music  Pictures  Projects  Public  Templates  Videos
┌──(kali㉿kali)-[~]
└─$ cd Downloads
┌──(kali㉿kali)-[~/Downloads]
└─$ dir
Addadshashanammu  Addadshashanammu.zip  enc_flag  file  flag  gemini-code-1787584453128.sh  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWmFWMDVHV2tkYVNHUlZDazFyY0ZkVWJGWlhZVlpLU0dWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
┌──(kali㉿kali)-[~/Downloads]
└─$ base64 -d
cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}
┌──(kali㉿kali)-[~/Downloads]
└─$ 
```

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 Big zip

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Unzip this archive and find the flag.

**Solución:** `picoCTF{gr3p_15_m4g1c_ef8790dc}`

**Código:** _(Debido al intento de lectura de texto directo de un ZIP, el formato imprimió salida binaria excesiva, la cual ha sido acortada para mantener el documento legible)._

Plaintext

```
PxP0PO▒OX;big-zip-files/foldersxabgsqxvb/file_tqlgpprzhlcrthhsuf.txtUT >^>^ux
0                                                                                                                                                ʻ
U^T09푸H3`é\{bǔ]HR1!-▒fS,vn;0B/gKHPxP0PO▒OX5big-zip-files/foldersxabgsqxvb/file_rcdeorbuexiv.txtUT       >^>^ux
... [Extensa salida binaria del zip corrupta impresa en pantalla] ...
U.eۀA"v}r%p3c#aZ*ʋE{▒2
P_IXkาPxP^JWobig-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/oldcrjwlmrdkpfnljxxlh.txtUT  >^>^ux
```

**Notas adicionales:** Siempre hay que verificar cómo escribir la bandera. **Referencias:**

## 🚩 First Find

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar? Unzip this archive and find the file named 'uber-secret.txt'

**Solución:** `picoCTF{f1nd_15_f457_ab443fd1}`

**Código:**

Bash

```
┌──(kali㉿kali)-[~/Downloads]
└─$ dir
Addadshashanammu  Addadshashanammu.zip  big-zip-files  big-zip-files.zip  enc_flag  file  files.zip  flag  gemini-code-1787584453128.sh  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
┌──(kali㉿kali)-[~/Downloads]
└─$ ls -s
total 7916
4 Addadshashanammu        36 big-zip-files         4 enc_flag  3904 files.zip     4 gemini-code-1787584453128.sh    20 static                       8 static.ltdis.x86_64.txt    20 warm
8 Addadshashanammu.zip  3112 big-zip-files.zip    16 file         4 flag          4 ltdis.sh                         4 static.ltdis.strings.txt   768 strings
┌──(kali㉿kali)-[~/Downloads]
└─$ ls -r
warm  strings  static.ltdis.x86_64.txt  static.ltdis.strings.txt  static  ltdis.sh  gemini-code-1787584453128.sh  flag  files.zip  file  enc_flag  big-zip-files.zip  big-zip-files  Addadshashanammu.zip  Addadshashanammu
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip files.zip
Archive:  files.zip
creating: files/
creating: files/satisfactory_books/
creating: files/satisfactory_books/more_books/
inflating: files/satisfactory_books/more_books/37121.txt.utf-8
inflating: files/satisfactory_books/23765.txt.utf-8
inflating: files/satisfactory_books/16021.txt.utf-8
inflating: files/13771.txt.utf-8
creating: files/adequate_books/
creating: files/adequate_books/more_books/
creating: files/adequate_books/more_books/.secret/
creating: files/adequate_books/more_books/.secret/deeper_secrets/
creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
inflating: files/adequate_books/more_books/1023.txt.utf-8
inflating: files/adequate_books/46804-0.txt
inflating: files/adequate_books/44578.txt.utf-8
creating: files/acceptable_books/
creating: files/acceptable_books/more_books/
inflating: files/acceptable_books/more_books/40723.txt.utf-8
inflating: files/acceptable_books/17880.txt.utf-8
inflating: files/acceptable_books/17879.txt.utf-8
inflating: files/14789.txt.utf-8   
┌──(kali㉿kali)-[~/Downloads]
└─$ find -name "uber-secret.txt"
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
┌──(kali㉿kali)-[~/Downloads]
└─$ cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
┌──(kali㉿kali)-[~/Downloads]
```