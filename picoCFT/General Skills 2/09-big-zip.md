## Big Zip
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)


Hints:
Can grep be instructed to look at every file in a directory and its subdirectories?




## Solución
```
Si esta en un archivo de texto se pone
picoCTF{gr3p_15_m4g1c_ef8790dc}
Desacrgamos el archivo
un zip
Y despues
grbau21-picoctf@webshell:~$ grep -R picoCTF
.python_history:'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
grep: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: binary file matches
README.txt:Welcome to the picoCTF webshell!
README.txt:picoCTF challenges.
README.txt:  Extensive brute-forcing is not necessary to solve picoCTF challenges.
README.txt:- If you change your username through the picoCTF website, you will
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
grbau21-picoctf@webshell:~$ 
```