
## Unminify
I don't like scrolling down to read the code of my website, so I've squished it. As a bonus, my pages load faster!Browse [here](http://titan.picoctf.net:61222/), and find the flag!


Hints:
1. Try CTRL+U / ⌘+U in your browser to view the page source. You can also add 'view-source:' before the URL, or try `curl <URL>` in your shell.
2. Minification reduces the size of code, but does not change its functionality.
3. What tools do developers use when working on a website? Many text editors and browsers include formatting.



## Solución:
```
Entrar al link:
http://titan.picoctf.net:61222/

Después Inspeccionar

(.venv) brisguz@DESKTOP-8V24E1B:~/Compiladores$ curl -s http://titan.picoctf.net:56566/ | grep -oE picoCTF{.*} --color=none | cut -d "\"" -f1
picoCTF{pr3tty_c0d3_51d374f0}


Flag: picoCTF{pr3tty_c0d3_51d374f0}
```
