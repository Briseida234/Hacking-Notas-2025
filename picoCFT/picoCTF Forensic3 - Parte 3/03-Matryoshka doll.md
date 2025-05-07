Las matrioskas son un conjunto de muñecas de madera de tamaño decreciente, colocadas una dentro de otra. ¿Cuál es la última? Imagen: [esta](https://mercury.picoctf.net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg)

#### Hints:
1. Espera, ¿se pueden ocultar archivos dentro de otros archivos? ¿Pero cómo encontrarlos?
2. Asegúrese de enviar la bandera como picoCTF{XXXXX}

## Solución:
```
1. Descargar 
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$ wget https://mercury.picoctf.
net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg
--2025-05-05 22:32:37--  https://mercury.picoctf.net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651630 (636K) [application/octet-stream]
Saving to: ‘dolls.jpg’

dolls.jpg            100%[===================>] 636.36K   224KB/s    in 2.8s

2025-05-05 22:32:41 (224 KB/s) - ‘dolls.jpg’ saved [651630/651630]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$



brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$ ls
dolls.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8

WARNING: Extractor.execute failed to run external extractor 'unzip -P '' -o '%e'': [Errno 2] No such file or directory: 'unzip', 'unzip -P '' -o '%e'' might not be installed correctly

WARNING: Extractor.execute failed to run external extractor 'jar xvf '%e'': [Errno 2] No such file or directory: 'jar', 'jar xvf '%e'' might not be installed correctly
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378950, uncompressed size: 383938, name: base_images/2_c.jpg
651608        0x9F158         End of Zip archive, footer length: 22

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$ ls
dolls.jpg  _dolls.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca$ cd _dolls.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted$ ls
4286C.zip  base_images
brisguz@DESKTOP-8V24E1B




brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted$ ls
4286C.zip  base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted$ unzip 4286C.zip
Archive:  4286C.zip
replace base_images/2_c.jpg? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: base_images/2_c.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted$ ls
4286C.zip  base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted$ cd base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images$ ls
2_c.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
383805        0x5DB3D         End of Zip archive, footer length: 22
383916        0x5DBAC         End of Zip archive, footer length: 22

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images$ ls
2_c.jpg  _2_c.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ unzip 2DD3B.zip
Archive:  2DD3B.zip
replace base_images/3_c.jpg? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: base_images/3_c.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ cd base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77651, uncompressed size: 79809, name: base_images/4_c.jpg
201423        0x312CF         End of Zip archive, footer length: 22

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg  _3_c.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extractedbrisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ ls1E2D6.zip  base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ cd base_images
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 65, uncompressed size: 81, name: flag.txt
79787         0x137AB         End of Zip archive, footer length: 22

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
brisguz@DESKTOP-8V24E1B:

```

```
-Por ultimo ver con un cat:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/muñeca/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt
picoCTF{4f11048e83ffc7d342a15bd2309b47de}brisguz@DESKTOP-8V24E1B:
```

#### Bandera

```
picoCTF{4f11048e83ffc7d342a15bd2309b47de}
```