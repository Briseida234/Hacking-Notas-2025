## Chrono

How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:
Server: saturn.picoctf.net
Port: 51588
Username: picoplayer 
Password: H9RmN0m18U


Hints:
1. (None)





## Solución:
```
grbau21-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 51588
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sun Feb 23 00:07:41 2025 from 3.140.102.47
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_d83baed1}
picoplayer@challenge:~$ 

```
