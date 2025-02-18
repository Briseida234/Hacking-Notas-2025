## Wave a flag
¿Puedes invocar indicadores de ayuda para una herramienta o un binario? [Este programa](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) tiene información extraordinariamente útil...


Hints:
1. Este programa solo funcionará en webshell o en otra computadora Linux.
2. Para que el archivo sea accesible en su shell, ingrese lo siguiente en el indicador de la Terminal:`$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`
3. Ejecute este programa ingresando lo siguiente en el indicador de terminal: `$ ./warm`, pero primero tendrá que hacerlo ejecutable con`$ chmod +x warm`
4. -h y --help son los argumentos más comunes que se dan a los programas para obtener más información de ellos.
5. No todos los programas implementan funciones de ayuda como -h y --help.


## Solución:
```
grbau21-picoctf@webshell:~$ 
grbau21-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2025-02-17 18:21:20--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                            100%[======================================================================================================>]  10.68K  --.-KB/s    in 0s      

2025-02-17 18:21:20 (294 MB/s) - 'warm' saved [10936/10936]

grbau21-picoctf@webshell:~$ chmod +x warm
grbau21-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
grbau21-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
grbau21-picoctf@webshell:~$ 
```
