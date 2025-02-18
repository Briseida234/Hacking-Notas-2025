## Strings It
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?

Hints:
[strings](https://linux.die.net/man/1/strings)



## Solución:
```
grbau21-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
--2025-02-18 03:50:02--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                         100%[======================================================================================================>] 757.84K  1.84MB/s    in 0.4s    

2025-02-18 03:50:02 (1.84 MB/s) - 'strings' saved [776032/776032]

grbau21-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_827aee91}
```
