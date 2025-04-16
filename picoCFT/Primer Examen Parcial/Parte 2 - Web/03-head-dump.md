
## Head-dump

Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.The website is running [picoCTF News](http://verbal-sleep.picoctf.net:61124/).


#### Hinst
1. Explore backend development with us
2. The head was dumped.


## Solución: 

```

Lleva a la página: http://verbal-sleep.picoctf.net:61124/


Entramos a la pagina web, y vemos lo que contiene, como a primera vista no vemos nada interesante, empezamos a dar clic en los links que nos encontramos. Ninguno nos lleva a nada interesante hasta que vemos la documentación [API]-Documentación (http://verbal-sleep.picoctf.net:61124/api-docs/)

Ahí vemos un poco de [[Métodos HTTP (Solicitudes al servidor)|solicitudes al servidor]], y vemos una que nos llama la atención, pues se llama como el problema (heapdump). Así que la ejecutamos donde esta un cuadrito(Try it out), y nos regresa un archivo; al abrirlo y buscar la palabra 'pico' encontramos la bandera.


Como Buscar en BlocNotas:
1. Edición
2. Buscar
3. Poner palabra: pico

picoCTF{Pat!3nt_15_Th3_K3y_46022a05}
```



#### Bandera
```
picoCTF{Pat!3nt_15_Th3_K3y_46022a05}
```

