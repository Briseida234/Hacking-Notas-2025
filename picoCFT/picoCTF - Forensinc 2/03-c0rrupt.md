
### c0rrupt

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.


#### Hints:
Try fixing the file header



## Solución:

```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/corrup$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
--2025-05-02 23:15:00--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 202940 (198K) [application/octet-stream]
Saving to: ‘mystery’

mystery                       100%[=================================================>] 198.18K   166KB/s    in 1.2s

2025-05-02 23:15:03 (166 KB/s) - ‘mystery’ saved [202940/202940]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for2/corrupt$ pngcheck -v mystery
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for2/corrupt$ xdg-open mystery
```

```
--Editar en hexedit y cambiar y luego abrir de nuevo la imagen
```

![[Pasted image 20250504220313.png]]


```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for2/corrupt$ file mystery
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced


-Abrir
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for2/corrupt$ xdg-open mystery
```

![[Pasted image 20250504220342.png]]


### Bandera:

```
picoCTF{c0rrupt10n_1847995}
```