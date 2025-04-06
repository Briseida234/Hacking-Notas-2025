
## Local Authority

Hints:
1. How is the password checked on this website?


## Solución:
```
Entrar y inspeccionar y network

function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}



Depues entrar con admin y esa contraseña
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
```