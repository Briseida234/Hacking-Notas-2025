## WhitePages
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!

#### Hints:
1. (None)




## Solución:

```
Crear carpeta
Desacegar archico
file whitepages.txt
cat whitepages.txt
xxd whitepages.txt
sed 's/°'



brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/whitpag$ wget https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
--2025-04-29 22:00:09--  https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2982 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt                100%[=================================================>]   2.91K  --.-KB/s    in 0s

2025-04-29 22:00:10 (17.5 MB/s) - ‘whitepages.txt’ saved [2982/2982]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/whitpag$




brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/whitpag$ python3 script.py

                picoCTF

                SEE PUBLIC RECORDS & BACKGROUND REPORT
                5000 Forbes Ave, Pittsburgh, PA 15213
                picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren2/whitpag$

```

#### Bandera:
```
picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}

```
