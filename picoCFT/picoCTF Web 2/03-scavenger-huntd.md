## Scavenger Huntd
Hay información interesante escondida en este sitio [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/) . ¿Puedes encontrarla?

Hints:
1. Deberías tener suficientes pistas para encontrar los archivos, no ejecutes un ataque de fuerza bruta.


## Solución
```


Flag: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}


Ver código fuente de la pagina
Primera Parte:
<!-- Here's the first part of the flag: picoCTF{t -->



Segunda Parte:
Entrar a  [mycss.css](http://mercury.picoctf.net:5080/mycss.css)
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */



Tercera Parte:
Entrar a "[myjs.js](http://mercury.picoctf.net:5080/myjs.js)"
http://mercury.picoctf.net:5080/
http://mercury.picoctf.net:5080/robots.txt
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?



Cuarta Parte:
Hay ciertos archivos que por defaul estan en un servidor apache
http://mercury.picoctf.net:5080/.htaccess
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.


Quinta Parte:
Existe  un archivo .DS_Store el cual almacena informacion de la 
confiuraxcion de una carpeta
http://mercury.picoctf.net:5080/.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _35844447}




picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}
```