## Based
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.



Hints:
1. I hear python can convert things.
2. It might help to have multiple windows open.


## Solución:
```
grbau21-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
oven
Please give the 01101111 01110110 01100101 01101110 as a word.
...
you have 45 seconds.....

Input:
oven
Please give me the  164 145 163 164 as a word.
Input:
test
Please give me the 7375626d6172696e65 as a word.
Input:
submarine
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```