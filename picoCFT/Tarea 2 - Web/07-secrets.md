

## Secrets
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:50162/).


Hints:
1. folders folders folders


## Solución

```
Entrar
http://saturn.picoctf.net:50162/

Entar a esta carpeta
http://saturn.picoctf.net:50162/secret/
Despues
http://saturn.picoctf.net:50162/secret/hidden/

Despues
http://saturn.picoctf.net:50162/secret/hidden/
Y ultima carpeta
http://saturn.picoctf.net:50162/secret/hidden/superhidden/


<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="mycss.css" />
  </head>

  <body>
    <h1>Finally. You found me. But can you see me</h1>
    <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_51b260fe}</h3>
  </body>
</html>



picoCTF{succ3ss_@h3n1c@10n_51b260fe}

```
