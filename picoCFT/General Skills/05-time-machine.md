## Time machine
¿En qué estaba trabajando por última vez? Recuerdo que escribí una nota para ayudarme a recordar...Puedes descargar los archivos del desafío aquí:

- [desafío.zip](https://artifacts.picoctf.net/c_titan/68/challenge.zip)


Hints:
1. El `cat`comando te permitirá leer un archivo, ¡pero eso no te ayudará aquí!
2. Lea el capítulo sobre Git de picoPrimer [aquí](https://primer.picoctf.org/#_git_version_control) .
3. Al confirmar un archivo con git, se puede (y se debe) incluir un mensaje.

## Solución:

```
grbau21-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/68/challenge.zip
--2025-02-22 21:05:11--  https://artifacts.picoctf.net/c_titan/68/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17738 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                   100%[======================================================================================================>]  17.32K  --.-KB/s    in 0.007s  

2025-02-22 21:05:11 (2.50 MB/s) - 'challenge.zip' saved [17738/17738]

grbau21-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
  inflating: drop-in/message.txt     
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
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
 extracting: drop-in/.git/objects/70/5ff639b7846418603a3272ab54536e01e3dc43  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
  inflating: drop-in/.git/logs/HEAD  
  inflating: drop-in/.git/logs/refs/heads/master


//Git init no
grbau21-picoctf@webshell:~$ cd drop-in
grbau21-picoctf@webshell:~/drop-in$ git log
grbau21-picoctf@webshell:~/drop-in$ 

picoCTF{t1m3m@ch1n3_b476ca06}

```
