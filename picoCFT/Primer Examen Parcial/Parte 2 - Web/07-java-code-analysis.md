
## Java Code Analysis!?!
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/482/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:54256/).


#### Hinst:
1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.








## Solución:
```

1. Ingresamos en la pagina y nos registramos para username:user y contrseña:user

2. Le damos en la parte de un cuadro que dice flag

3. Insepccionar y en aplication
* Ahí ir a storange
* Despues en Local storange y el link de abajo



4. Copiar cookie
-En auth-token copiar valor

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc0NTQzNTYwNiwiaWF0IjoxNzQ0ODMwODA2LCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.WHomoz9KI7XuimuHBrFMzHDdawvCPFV5zBStbI0ne1c






5. Ir a convertirla jwt.io
Nos apoyamos de [jwt token editor](https://jwt.io/), y modificamos tanto la contraseña (a 1234), el usuario y el rol (Admin), así como el userID(2) y email(admin) . Y nos da este nuevo token:


eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDU0MzU2MDYsImlhdCI6MTc0NDgzMDgwNiwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.DKELjsuRUWIUpxn9F6sYyHdAEik_PgI8NauUEYnN9Kw




```

De esta forma modificarlo y de ahí te dará el nuevo valor de la cookie:

![[Pasted image 20250416134348.png]]




```

6. Después el nuevo valor modificarlo y ponerlo dentro de la pagina web, esta es la cookie:

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDU0MzU2MDYsImlhdCI6MTc0NDgzMDgwNiwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.DKELjsuRUWIUpxn9F6sYyHdAEik_PgI8NauUEYnN9Kw





7. Tambien modifica el payload, de esta forma, como lo modificaste en el paso 5 y luego actualizas la pagina, depues de tener los dos valores modificados

{"role":"Admin","iss":"bookshelf","exp":1745435606,"iat":1744830806,"userId":2,"email":"admin"}





8. Te dara la  bandera
picoCTF{w34k_jwt_n0t_g00d_d72df65e}



```



![[Pasted image 20250416133537.png]]


#### Bandera

```
picoCTF{w34k_jwt_n0t_g00d_d72df65e}

```






