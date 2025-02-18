## 2Warm

Can you convert the number 42 (base 10) to binary (base 2)?

Hints:
1. Submit your answer in our competition's flag format. For example, if your answer was '11111', you would submit 'picoCTF{11111}' as the flag.


## Solución 1:
* Usando Python
```
>>> bin(42)
'0b101010'
>>> bin(42)[2:]
'101010'
>>>
picoCTF{101010}
```

## Solución 2
* Usando cyberchef

```
Input: 42
Recipe:
From Decimal
To Binary: Byte Length: 6

Outpout: 101010
```

