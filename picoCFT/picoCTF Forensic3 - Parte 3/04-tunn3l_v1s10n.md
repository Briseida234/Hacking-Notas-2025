Encontramos este [archivo](https://mercury.picoctf.net/static/da18eed3d15fd04f7b076bdcecf15b27/tunn3l_v1s10n) . Recupera la bandera.


#### Hints:
1. Es extraño que no se muestre correctamente...

## Solución:

```
1. Descargar
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$ wget https://mercury.picoctf.net/static/da18eed3d15fd04f7b076bdcecf15b27/tunn3l_v1s10n
--2025-05-06 07:35:13--  https://mercury.picoctf.net/static/da18eed3d15fd04f7b076bdcecf15b27/tunn3l_v1s10n
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n        100%[=====================>]   2.76M  1.91MB/s    in 1.4s

2025-05-06 07:35:16 (1.91 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$
```



```

2. Cambiar extensión
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$ cp tunn3l_v1s10n flag.bmp

```


```
3. Modificar el archivo en hexedit, con la nueva extensión
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$ hexedit flag.bmp
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$
```
![[Pasted image 20250506161610.png]]


```
4. Abrir el archivo

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/tunn$ xdg-open flag.bmp
picoCTF{qu1t3_a_v13w_2020}
```

![[Pasted image 20250506161351.png]]
#### Bandera
```
picoCTF{qu1t3_a_v13w_2020}
```