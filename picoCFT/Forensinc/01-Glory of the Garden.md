
## Glory of the Garden
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

Hints:
1. What is a hex editor?

## Solución:

```
Usando strings -n18 garden.jpg



brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/garden$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2025-04-08 12:37:33--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg                    100%[=================================================>]   2.19M   559KB/s    in 4.0s

2025-04-08 12:37:38 (559 KB/s) - ‘garden.jpg’ saved [2295192/2295192]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/garden$


Parte 2:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/garden$ strings -n18 garden.jpg
Copyright (c) 1998 Hewlett-Packard Company
IEC http://www.iec.ch
IEC http://www.iec.ch
.IEC 61966-2.1 Default RGB colour space - sRGB
.IEC 61966-2.1 Default RGB colour space - sRGB
,Reference Viewing Condition in IEC61966-2.1
,Reference Viewing Condition in IEC61966-2.1
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/garden$


Flag: picoCTF{more_than_m33ts_the_3y33dd2eEF5}

```