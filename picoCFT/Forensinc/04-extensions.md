## Extensions
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?-

Hints:
1. How do operating systems know what kind of file it is? (It's not just the ending!
2. Make sure to submit the flag as picoCTF{XXXXX}


## Solución:

 ```
 wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
--2025-04-07 12:52:17--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt                         100%[==========================================================>]   9.75K  --.-KB/s    in 0s

2025-04-07 12:52:18 (20.6 MB/s) - ‘flag.txt’ saved [9984/9984]


Parte Dos:
Cambiar extensión
mv flag.txt

 mv flag.txt flag.png
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/extensions$ ls
flag.png

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/extensions$ eog flag.png

Flag: picoCTF{now_you_know_about_extensions}
 ```





![[Pasted image 20250407130046.png]]