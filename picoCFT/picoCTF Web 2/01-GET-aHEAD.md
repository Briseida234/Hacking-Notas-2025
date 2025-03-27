
## GET aHEAD

Encuentra la bandera que se encuentra en este servidor para adelantarte a la competencia [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

Hints:
1. Quizás tengas más de 2 opciones
2. Consulta herramientas como Burpsuite para modificar tus solicitudes y ver las respuestas.



## Solución

```

--Usar para encontrar:  curl -I http://mercury.picoctf.net:45028/index.php?

---------
brisguz@DESKTOP-8V24E1B:~$ curl -X GET http://mercury.picoctf.net:45028/index.php?

<!doctype html>
<html>
<head>
    <title>Red</title>
    <link rel="stylesheet" type="text/css" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
        <style>body {background-color: red;}</style>
</head>
        <body>
                <div class="container">
                        <div class="row">
                                <div class="col-md-6">
                                        <div class="panel panel-primary" style="margin-top:50px">
                                                <div class="panel-heading">
                                                        <h3 class="panel-title" style="color:red">Red</h3>
                                                </div>
                                                <div class="panel-body">
                                                        <form action="index.php" method="GET">
                                                                <input type="submit" value="Choose Red"/>
                                                        </form>
                                                </div>
                                        </div>
                                </div>
                                <div class="col-md-6">
                                        <div class="panel panel-primary" style="margin-top:50px">
                                                <div class="panel-heading">
                                                        <h3 class="panel-title" style="color:blue">Blue</h3>
                                                </div>
                                                <div class="panel-body">
                                                        <form action="index.php" method="POST">
                                                                <input type="submit" value="Choose Blue"/>
                                                        </form>
                                                </div>
                                        </div>
                                </div>
                        </div>
                </div>
        </body>
</html>
brisguz@DESKTOP-8V24E1B:~$



brisguz@DESKTOP-8V24E1B:~$ curl -I http://mercury.picoctf.net:45028/index.php?
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8


picoCTF{r3j3ct_th3_du4l1ty_775f2530}

```