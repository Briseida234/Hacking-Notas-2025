## Python Wrangling

#### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py) using [this password](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/pw.txt) to get [the flag](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en)?


Hints:
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py`
2. $ man python



## Solución: 
```
1. Descargamos los tres archivos con wget:
 * wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py
 * wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac9
 * wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en



grbau21-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py
--2025-04-15 20:06:07--  https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: 'ende.py'

ende.py                 100%[============================>]   1.30K  --.-KB/s    in 0s      

2025-04-15 20:06:07 (425 MB/s) - 'ende.py' saved [1328/1328]

grbau21-picoctf@webshell:~$ 





2. Checamos esto:
grbau21-picoctf@webshell:~$ python3 ende.py -h
Usage: ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'
grbau21-picoctf@webshell:~$ 



3. Vemos la contraseña que eta dentro de px.txt con un cat
grbau21-picoctf@webshell:~$ cat pw.txt
68f88f9368f88f9368f88f9368f88f93
grbau21-picoctf@webshell:~$



4. Corremos el programa y ingresamos la contraseña al que le hicimos el cat(pw.txt) y dara la flag
grbau21-picoctf@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:68f88f9368f88f9368f88f9368f88f93
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}
grbau21-picoctf@webshell:~$ 




Flag: picoCTF{4p0110_1n_7h3_h0us3_68f88f93}

```