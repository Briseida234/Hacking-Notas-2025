## PW Crack 3
¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/17/level3.py) y necesitará la [bandera](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) cifrada y el [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) en el mismo directorio también.Hay 7 contraseñas posibles, de las cuales 1 es correcta. Puedes encontrarlas examinando el script de verificación de contraseñas.


Hints:
1. Para ver el archivo level3.hash.bin en el webshell, haga lo siguiente:`$ bvi level3.hash.bin`
2. Para salir `bvi`escriba `:q`y presione enter.
3. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.
## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2025-02-20 01:24:05--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                       100%[======================================================================================================>]   1.31K  --.-KB/s    in 0s      

2025-02-20 01:24:05 (14.4 MB/s) - 'level3.py' saved [1337/1337]

grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2025-02-20 01:24:24--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                             100%[======================================================================================================>]      31  --.-KB/s    in 0s      

2025-02-20 01:24:25 (2.33 MB/s) - 'level3.flag.txt.enc' saved [31/31]

grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2025-02-20 01:24:40--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                 100%[======================================================================================================>]      16  --.-KB/s    in 0s      

2025-02-20 01:24:40 (4.33 MB/s) - 'level3.hash.bin' saved [16/16]

grbau21-picoctf@webshell:~$ bvi level3.hash.bin

bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
grbau21-picoctf@webshell:~$ 


Ahora contrsaeña posible
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

Contraseña:
87ab
grbau21-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
grbau21-picoctf@webshell:~$ 



```