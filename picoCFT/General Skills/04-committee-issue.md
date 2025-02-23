## Committee issue

Accidentalmente escribí la bandera. ¡Qué bueno que la borré!Puedes descargar los archivos del desafío aquí:

- [desafío.zip](https://artifacts.picoctf.net/c_titan/77/challenge.zip)

Hints:
1. ¡El control de versiones puede ayudarte a recuperar archivos si los modificas o los pierdes!
2. Lee el capítulo sobre Git de picoPrimer [aquí](https://primer.picoctf.org/#_git_version_control)
3. Puedes 'extraer' confirmaciones para ver los archivos dentro de ellas

## Solución:

```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/77/challenge.zip
--2025-02-22 22:12:49--  https://artifacts.picoctf.net/c_titan/77/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19199 (19K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                   100%[======================================================================================================>]  18.75K  --.-KB/s    in 0.006s  

2025-02-22 22:12:49 (3.22 MB/s) - 'challenge.zip' saved [19199/19199]

grbau21-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
replace drop-in/.git/description? [y]es, [n]o, [A]ll, [N]one, [r]ename: All
  inflating: drop-in/.git/description  
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
  inflating: drop-in/.git/info/exclude  
 extracting: drop-in/.git/refs/heads/master  
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/96/
 extracting: drop-in/.git/objects/96/f7309de67d785ec0b93b8766ff2882bef5c3ef  
 extracting: drop-in/.git/objects/8c/1d254e2da6713e33acd6d622fc1dae357ec3c6  
 extracting: drop-in/.git/objects/3d/5ec8a26ee7b092a1760fea18f384c35e435139  
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
 extracting: drop-in/.git/objects/e1/237df82d2e69f62dd53279abc1c8aeb66f6d64  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
  inflating: drop-in/.git/logs/HEAD  
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
grbau21-picoctf@webshell:~$ cd drop-in/
grbau21-picoctf@webshell:~/drop-in$ ls -agit log
ls: cannot access 'log': No such file or directory
grbau21-picoctf@webshell:~/drop-in$ ls
flag.py  message.py  message.txt
grbau21-picoctf@webshell:~/drop-in$ cat message.txt
TOP SECRET


--Ahora
grbau21-picoctf@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/grbau21-picoctf/drop-in/.git/
grbau21-picoctf@webshell:~/drop-in$ git log
grbau21-picoctf@webshell:~/drop-in$ 
grbau21-picoctf@webshell:~/drop-in$ git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139
Previous HEAD position was e1237df remove sensitive info
HEAD is now at 3d5ec8a create flag
grbau21-picoctf@webshell:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_30e86d36}
grbau21-picoctf@webshell:~/drop-in$ 


```
