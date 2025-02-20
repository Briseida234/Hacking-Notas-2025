## PW Crack 2
¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/13/level2.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) cifrada en el mismo directorio.

Hints:
1. ¿Te resulta familiar esta codificación?
2. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.
## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.py
--2025-02-20 01:17:27--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                       100%[======================================================================================================>]     914  --.-KB/s    in 0s      

2025-02-20 01:17:27 (40.9 MB/s) - 'level2.py' saved [914/914]

grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2025-02-20 01:17:42--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                             100%[======================================================================================================>]      31  --.-KB/s    in 0.001s  

2025-02-20 01:17:42 (47.3 KB/s) - 'level2.flag.txt.enc' saved [31/31]

grbau21-picoctf@webshell:~$ nano level2.py
grbau21-picoctf@webshell:~$ paython
-bash: paython: command not found
grbau21-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
>>> 

Despues ingresar esa contraseña que esta en el codigo 

grbau21-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: de76 
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
grbau21-picoctf@webshell:~$ 
```