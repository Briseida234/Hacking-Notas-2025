## m00nwalk
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

#### Hints:
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option



## Solución:
```
1. Crear carpeta moonn
2. Descargar archivo


SSTV-Para sustraer la imagen del audio
Ir a:
cd /opt
sudo git clone https://github.com/colaclanth/sstv.git
ls
cd sstv
python setup.py install
sstv
sstv -d message.wav -o flag.png
open flag.png



-Crear una carpeta y descargar el archivo
Primer paso:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$ wget https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav
--2025-04-29 21:32:23--  https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’

message.wav                   100%[=================================================>]  10.55M  1.53MB/s    in 7.7s

2025-04-29 21:32:31 (1.37 MB/s) - ‘message.wav’ saved [11066998/11066998]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$




Segundo Paso:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$ cd /opt


Tercer Paso:
brisguz@DESKTOP-8V24E1B:/opt$ sudo git clone https://github.com/colaclanth/sstv.git
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Counting objects: 100% (59/59), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 221 (delta 51), reused 49 (delta 49), pack-reused 162 (from 1)
Receiving objects: 100% (221/221), 1.01 MiB | 156.00 KiB/s, done.
Resolving deltas: 100% (139/139), done.
brisguz@DESKTOP-8V24E1B:/opt$


Cuarto Paso:
-Instalar herramienta
-Decodificar audio y a imagen

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [######################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$


5. Checar la descarga y abrir la imagen
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$ ls
message.wav  result.png
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/monwalk$ xdg-open result.png



picoCTF{beep_boop_im_in_space}

```


#### Bandera:

```
picoCTF{beep_boop_im_in_space}
```
