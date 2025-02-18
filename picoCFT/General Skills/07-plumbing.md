
## Plumbing
A veces es necesario manejar datos de procesos fuera de un archivo. ¿Puedes encontrar una forma de conservar la salida de este programa y buscar la bandera? Conéctate a `jupiter.challenges.picoctf.org 14291`.

Hits
1. Recuerde que el formato de la bandera es picoCTF{XXXX}
2. ¿Qué es una pipa? No, no ese tipo de pipa... Este [tipo](http://www.linfo.org/pipes.html)
## Solución
* El salida es para mandarlo a un archivo y guardar
```
nc jupiter.challenges.picoctf.org 14291
 nc jupiter.challenges.picoctf.org 14291 > salida
^C
grbau21-picoctf@webshell:~$ cat salida | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
```