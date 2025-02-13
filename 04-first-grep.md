## First Grep
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.


Hints: 
1. grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php) 


## Solución 1:
```
grbau21-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
--2025-02-12 18:43:48--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file.1'

file.1                                          100%[======================================================================================================>]  14.21K  --.-KB/s    in 0s      

2025-02-12 18:43:48 (399 MB/s) - 'file.1' saved [14551/14551]
```


## Solución 2:
```
grbau21-picoctf@webshell:~$ cat file.1 | grep pico
picoCTF{grep_is_good_to_find_things_f77e0797}
```
