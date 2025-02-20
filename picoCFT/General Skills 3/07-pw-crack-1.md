## PW Crack 1
¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/12/level1.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) cifrada en el mismo directorio.

Hints:
1. Para ver el archivo en el webshell, haga lo siguiente:`$ nano level1.py`
2. Para salir `nano`, presione Ctrl y x y siga las instrucciones en pantalla.
3. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.

## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2025-02-20 01:10:21--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                       100%[======================================================================================================>]     876  --.-KB/s    in 0s      

2025-02-20 01:10:21 (58.8 MB/s) - 'level1.py' saved [876/876]

grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2025-02-20 01:10:41--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                             100%[======================================================================================================>]      30  --.-KB/s    in 0s      

2025-02-20 01:10:42 (1.56 MB/s) - 'level1.flag.txt.enc' saved [30/30]

grbau21-picoctf@webshell:~$ nano level1.py
grbau21-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
grbau21-picoctf@webshell:~$
```