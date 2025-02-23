## Bases
¿Qué `bDNhcm5fdGgzX3IwcDM1`significa esto? Creo que tiene algo que ver con las bases.


Hints:
1. Envíe su respuesta en nuestro formato de bandera. Por ejemplo, si su respuesta fue "hola", deberá enviar "picoCTF{hola}" como bandera.


## Solución 1
* Usando Cyberchef
```
Input: bDNhcm5fdGgzX3IwcDM1
Recipe: From Base64
Output: l3arn_th3_r0p35
picoCTF{l3arn_th3_r0p35}
```



## Solución 2
```
grbau21-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
l3arn_th3_r0p35grbau21-picoctf@webshell:~$ 
picoCTF{l3arn_th3_r0p35}
```



## Solución 3
* Usando python
```
 python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
>>> 
```
