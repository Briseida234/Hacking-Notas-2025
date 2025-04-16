
## Java Code Analysis!?!
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/482/bookshelf-pico.zip).


#### Hinst:
1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.








## Solución:
```

1. Ingresamos en la pagina y nos registramos

2. Le damos en la parte de un cuadro que dice flag

3. Insepccionar y en aplication


4. Copiar cookie
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc0NTM4NDk4MiwiaWF0IjoxNzQ0NzgwMTgyLCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.REgTLnhvnra2fTNnuyLzxSGI34yCtwLc5OdZsLkaPNk


5. Ir a convertirla jwt.io
Nos apoyamos de [jwt token editor](https://jwt.io/), y modificamos tanto la contraseña (a 1234), el usuario y el rol (admin), así como el userID(2). Y nos da este nuevo token:




6. Después el nuevo valor modificarlo y actualizar

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDUzODQ5ODIsImlhdCI6MTc0NDc4MDE4MiwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.V0VpQj-61PoAAyGmAFfLnbVkgtSmtbFXhsT71IExZUw



7. Te dara la  bandera

```



#### Bandera

```


```



