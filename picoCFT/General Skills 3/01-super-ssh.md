## Super SSH
Using a Secure Shell (SSH) is going to be pretty important.
Additional details will be available after launching your challenge instance.

El uso de un Secure Shell (SSH) será bastante importante.¿ Puedes `ssh`ir al puerto para conseguir la bandera?`ctf-player``titan.picoctf.net``50186`También necesitarás la contraseña `1db87a14`. Si te la piden, acepta la huella digital con `yes`.Si su dispositivo no tiene un shell, puede usar: [https://webshell.picoctf.org](https://webshell.picoctf.org/)Si no está seguro de qué es un shell, consulte nuestro manual básico: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)

Hints:
1. [https://linux.die.net/man/1/ssh](https://linux.die.net/man/1/ssh)
2.  You can try logging in 'as' someone with `<user>`@titan.picoctf.net
3. How could you specify the port?
4. Remember, passwords are hidden when typed into the shell
## Solución:
```
grbau21-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 53006
The authenticity of host '[titan.picoctf.net]:53006 ([3.139.174.234]:53006)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:53006' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_45a48857}
Connection to titan.picoctf.net closed.
grbau21-picoctf@webshell:~$ 
```

