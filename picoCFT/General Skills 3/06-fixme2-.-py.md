## Fixme2.py
Corrija el error de sintaxis en el script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/4/fixme2.py)

Hints:
1. ¿Igualdad y asignación son el mismo símbolo?
2. Para ver el archivo en el webshell, haga lo siguiente:`$ nano fixme2.py`
3. Para salir `nano`, presione Ctrl y x y siga las instrucciones en pantalla.
4. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.

## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2025-02-20 00:30:51--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                       100%[======================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-02-20 00:30:51 (208 MB/s) - 'fixme2.py' saved [1029/1029]

grbau21-picoctf@webshell:~$ nano fixme2.py
grbau21-picoctf@webshell:~$ python3 fixme2.py
  File "/home/grbau21-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

grbau21-picoctf@webshell:~$ nano fixme2.py
grbau21-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
grbau21-picoctf@webshell:~$ 
```