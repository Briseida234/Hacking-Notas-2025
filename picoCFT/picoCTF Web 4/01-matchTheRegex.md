
## MatchTheRegex

How about trying to match a regular expressionThe website is running [here](http://saturn.picoctf.net:64782/).



Hints:
1. Access the webpage and try to match the regular expression associated with the text field



## Solución:

```
//Nos ayida  a valida
https://regexr.com

picoCTF{succ3ssfully_matchtheregex_f89ea585}
Entrar al ver código fuente y copear la expresión que nos pueda validar
```


![[Pasted image 20250402121724.png]]




```

Expresión: ^p.....F!?
Entrar a:  https://regexr.com

Poner:
picoCTF
p12345F


Significa que hay una p, cuatro caracteres y una F y después de ahí no importa lo que haya

Flag: picoCTF{succ3ssfully_matchtheregex_f89ea585}

```