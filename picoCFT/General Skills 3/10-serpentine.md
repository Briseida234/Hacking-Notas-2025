## Serpentine
¡Encuentra la bandera en el script de Python![Descargar script de Python](https://artifacts.picoctf.net/c/35/serpentine.py)



Hints:
1. Intente ejecutar el script y vea qué sucede.
2.  En el webshell, intente examinar el script con un editor de texto como`nano`
3. Para salir `nano`, presione Ctrl y x y siga las instrucciones en pantalla.
4. `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.
## Solución:
```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2025-02-20 04:17:55--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py                                   100%[======================================================================================================>]   2.49K  --.-KB/s    in 0s      

2025-02-20 04:17:55 (154 MB/s) - 'serpentine.py' saved [2550/2550]

grbau21-picoctf@webshell:~$ python3 serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
Look how far you've come!
-----------------------------------------------------

Ahora quitar la mitad del codigo y llamar la funcion 

What would you like to do? (a/b/c) c
grbau21-picoctf@webshell:~$ nano serpentine.py
grbau21-picoctf@webshell:~$ python3 serpentine.py
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
grbau21-picoctf@webshell:~$ 


```
