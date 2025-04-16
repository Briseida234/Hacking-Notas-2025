## Cookie Monster Secret Recipe
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:51173/) and good luck



#### Hints:
1. Sometimes, the most important information is hidden in plain sight. Have you checked all parts of the webpage?
2. Cookies aren't just for eating - they're also used in web technologies!
3. Web browsers often have tools that can help you inspect various aspects of a webpage, including things you can't see directly.



## Solución:
```
1. Entrar a la página web
http://verbal-sleep.picoctf.net:51173/

2. Registrase en la pagina 




3. Despues Copiar la cookie obtenida y convertir:

cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzA1N0JDQjUxfQ%3D%3D






4. Convertir cookie usando cyberchef

Recipe: From Base64
Input: cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzA1N0JDQjUxfQ%3D%3D
Output: picoCTF{c00k1e_m0nster_l0ves_c00kies_057BCB51}
ÃÜ

```


#### Bandera
```

picoCTF{c00k1e_m0nster_l0ves_c00kies_057BCB51}

```
