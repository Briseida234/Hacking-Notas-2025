## Runme.py
Ejecute el `runme.py`script para obtener la bandera. Descargue el script con su navegador o con `wget`el shell web.[Descargar el script Python runme.py](https://artifacts.picoctf.net/c/34/runme.py)



Hints:
1. Si tienes Python en tu computadora, puedes descargar el script normalmente y ejecutarlo. De lo contrario, usa el `wget`comando en el shell web.
2. Para utilizarlo `wget`en el webshell, primero haga clic derecho en el enlace de descarga y seleccione 'Copiar enlace' o 'Copiar dirección de enlace'
3. Escribe todo lo que aparece después del signo de dólar en el webshell: `$ wget` , luego pega el enlace después del espacio `wget`y presiona Enter. ¡Esto descargará el script en el webshell para que puedas ejecutarlo!
4. Finalmente, para ejecutar el script, escribe todo lo que está después del signo de dólar y luego presiona Enter: ¡ `$ python3 runme.py`Ahora deberías tener la bandera!


## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-02-20 04:11:05--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                        100%[======================================================================================================>]     270  --.-KB/s    in 0s      

2025-02-20 04:11:05 (4.15 MB/s) - 'runme.py' saved [270/270]

grbau21-picoctf@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
grbau21-picoctf@webshell:~$

```