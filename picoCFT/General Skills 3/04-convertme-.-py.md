## Convertme.py
Ejecute el script de Python y convierta el número dado de decimal a binario para obtener la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/23/convertme.py)

Hints:
1. ¡Busca una aplicación de conversión de números decimales a binarios en la web o usa la calculadora de tu computadora!
2. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.
3. Si tienes Python en tu computadora, puedes descargar el script normalmente y ejecutarlo. De lo contrario, usa el `wget`comando en el shell web.
4. Para utilizarlo `wget`en el webshell, primero haga clic derecho en el enlace de descarga y seleccione 'Copiar enlace' o 'Copiar dirección de enlace'
5. Escribe todo lo que aparece después del signo de dólar en el webshell: `$ wget` , luego pega el enlace después del espacio `wget`y presiona Enter. ¡Esto descargará el script en el webshell para que puedas ejecutarlo!
6. Por último, para ejecutar el script, escriba todo lo que está después del signo de dólar y luego presione Enter:`$ python3 convertme.py`

## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2025-02-20 03:03:52--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                    100%[======================================================================================================>]   1.16K  --.-KB/s    in 0s      

2025-02-20 03:03:52 (430 MB/s) - 'convertme.py' saved [1189/1189]

grbau21-picoctf@webshell:~$ python3 convertme.py
If 97 is in decimal base, what is it in binary base?
Answer: 01100001
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
grbau21-picoctf@webshell:~$ 


En Cyberchef
Input:97
Recipe: From Decimal
To Binary
Output:
01100001


```