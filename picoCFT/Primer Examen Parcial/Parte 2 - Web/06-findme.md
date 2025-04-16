
## findme

Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:51579/).
#### Hints:
1. any redirections?


## Solución
```
1. Nos dirigimos a la página
2. Ingresamos como Username: test y password: test!
http://saturn.picoctf.net:51579/home


3. Ingresar a nuestro historial y vemos que hay dos flag  y le damos copiar dirección del vinculo a las 2
http://saturn.picoctf.net:51579/next-page/id=bF90aGVfd2F5XzAxZTc0OGRifQ==

http://saturn.picoctf.net:51579/next-page/id=cGljb0NURntwcm94aWVzX2Fs




4. Copeamos solamente el ID

bF90aGVfd2F5XzAxZTc0OGRifQ==
cGljb0NURntwcm94aWVzX2Fs



5. Decodificar  lo del paso 4 usando cyberchef, obteniendo la bandera por partes

Recipe: From Base64
Input: bF90aGVfd2F5XzAxZTc0OGRifQ==
Output: l_the_way_01e748db}


Recipe:  From Bae64
Input: cGljb0NURntwcm94aWVzX2Fs
Output: picoCTF{proxies_al


6. Bandera Completa:
picoCTF{proxies_all_the_way_01e748db}




Flag: picoCTF{proxies_all_the_way_01e748db}


```