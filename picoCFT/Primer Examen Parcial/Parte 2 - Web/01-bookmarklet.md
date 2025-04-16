
## Bookmarklet

Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:58206/), and find the flag!


#### Hints:
1. A bookmarklet is a bookmark that runs JavaScript instead of loading a webpage.
2. What happens when you click a bookmarklet?
3. Web browsers have other ways to run JavaScript too.




## Solución:
```
1. Primero ingresamos a la pagina web y encontramos un código de [[Javascript]]:

  javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÉÕËÆÒÇÚËí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    


2.  Este código, como nos sugería la pista, lo ejecutamos en la consola de la pagina web y ingresamos en consola y ponemos el código:

allow pasting
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£Ö�ÓÚåÛÑ¢ÕÓ�¡��ÒÅ¤�í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    


3.  Esto nos genera una alerta, que nos regresa la bandera.
picoCTF{p@g3_turn3r_cebccdfe}



```


#### Bandera

```
picoCTF{p@g3_turn3r_cebccdfe}
```