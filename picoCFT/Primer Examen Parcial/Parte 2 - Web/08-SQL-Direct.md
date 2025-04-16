
## SQL Direct
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 51895 -U postgres pico`Password is `postgres`



#### Hinst:
What does a SQL database contain?


## Solución: 

```

1. Nos conectamos a :   'psql -h saturn.picoctf.net -p 51895 -U postgres pico' y ingresamos la contraseña que da

grbau21-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 51895 -U postgres pico
Password for user postgres: 
psql (14.17 (Ubuntu 14.17-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.





2. Utilizamos el comando '\l' para listar todas las bases de datos 

pico=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
-----------+----------+----------+------------+------------+-----------------------
 pico      | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(4 rows)

pico=# 





3. Nos reconectamos a la base de datos pico con '\c pico'
//Reconectarse

pico=# \c pico
psql (14.17 (Ubuntu 14.17-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
You are now connected to database "pico" as user "postgres".
pico=# 





4. Este comando "\dt", mostrara todas las tablas

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# 





5. En la tabla anterior del paso 4 hay una tabla con nombre 'flgas', ahora hacerle un select a esa tabla

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 






Flag: picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}


```