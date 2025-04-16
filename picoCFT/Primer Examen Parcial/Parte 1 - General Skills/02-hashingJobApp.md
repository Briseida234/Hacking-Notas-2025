
## HashingJobApp

#### Description
If you want to hash with the best, beat this test!`nc saturn.picoctf.net 55775`


Hints:
1. You can use a commandline tool or web app to hash text
2. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.



## Solución:

```
1. Vamos a conectarnos: nc saturn.picoctf.net 55775
2. Vamos a convertir la palabra que esta entre comillas en la terminal a MD5 como dice el ejercicio usando cyberchef y el resultado lo ponderemos en answer
3. Link para convertir de la palabra a MD5

https://gchq.github.io/CyberChef/#recipe=MD5()


brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/hashingapp$ nc saturn.picoctf.net 55775
Please md5 hash the text between quotes, excluding the quotes: 'a high school bathroom'
Answer:
98219c442a477b6dc1756d2a6d49d8df
98219c442a477b6dc1756d2a6d49d8df
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'hair transplants'
Answer:
5b416c0db26c7e0478766fc51931a3ab
5b416c0db26c7e0478766fc51931a3ab
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'coconuts'
Answer:
78d1999482f432e9c229269151140542
78d1999482f432e9c229269151140542
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}





* Usando Cyberchef
Input: a high school bathroom
Recipe: MD5
Output: 98219c442a477b6dc1756d2a6d49d8df


Input: hair transplants
Recipe: MD5
Output: 5b416c0db26c7e0478766fc51931a3ab


Input: coconuts
Recipe: MD5
Output: 78d1999482f432e9c229269151140542


Flag: picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}

```