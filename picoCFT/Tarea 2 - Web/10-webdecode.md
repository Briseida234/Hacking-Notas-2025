Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:63934/) to find the flag

## WebDecode

Hints:
1. Use the web inspector on other files included by the web page.
2. The flag may or may not be encoded


## Solución:
```
http://titan.picoctf.net:63934/
Ver codigo fuente

Depues aqui
view-source:http://titan.picoctf.net:63934/


Después en el código entrar about.htm
http://titan.picoctf.net:63934/about.html


<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9">
   <h1>
    Try inspecting the page!! You might find it there
   </h1>
   <!-- .about-container -->
  </section>



Usando Cyberchef:
Input:cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9
Recipe: From Base64
Output: picoCTF{web_succ3ssfully_d3c0ded_df0da727}
```