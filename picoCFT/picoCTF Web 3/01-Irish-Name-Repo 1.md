Cuando hay un login hay una base de datos
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!


Hints:
1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.


## Solución
```
https://jupiter.challenges.picoctf.org/problem/33850/login.html
Ver codigo fuente o inspeccionar



Poniendo
** Con la Inyección SQL ** 

admin'--   Porque no importa que hay después
hola
o
juan' or 1=1;  De que es verdadero

# ¡Has iniciado sesión!

Tu bandera es: picoCTF{s0m3_SQL_f8adf3fb}

```