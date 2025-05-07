

### WebNet0
Encontramos esta [captura de paquete](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) y [la clave](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key) . Recuperar la bandera.

#### Hints:
1. Intente utilizar una herramienta como Wireshark.
2. ¿Cómo se puede descifrar la transmisión TLS?

## Solución:

-Usando la terminal
-Descargar archivos
```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/web0$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
--2025-05-05 21:56:09--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13163 (13K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                  100%[=================================================>]  12.85K  --.-KB/s    in 0.001s

2025-05-05 21:56:11 (22.4 MB/s) - ‘capture.pcap’ saved [13163/13163]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/web0$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
--2025-05-05 21:56:25--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                  100%[=================================================>]   1.66K  --.-KB/s    in 0s

2025-05-05 21:56:27 (22.5 MB/s) - ‘picopico.key’ saved [1704/1704]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/web0$

```




--Ver comando con ssldump
```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/web0$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
--
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for3/web0$


```
#### Bandera
```
picoCTF{nongshim.shrimp.crackers}
```
