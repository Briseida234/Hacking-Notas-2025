## Specialer


Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 63953 ctf-player@saturn.picoctf.net`. The password is `3f39b042`


Hints:
1. What programs do you have access to?



## Solución
```
1.  Conectarse
ssh -p 63953 ctf-player@saturn.picoctf.net

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/specialer$ ssh -p 63953 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:63953 ([13.59.203.175]:63953)' can't be established.
ED25519 key fingerprint is SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
    ~/.ssh/known_hosts:3: [hashed name]
    ~/.ssh/known_hosts:4: [hashed name]
    ~/.ssh/known_hosts:5: [hashed name]
    ~/.ssh/known_hosts:6: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:63953' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password:
Permission denied, please try again.
ctf-player@saturn.picoctf.net's password:
Specialer$




//AQUI

2. Primero: cd ../..  y tab2


3. Después se pone asi:  cd ../../ y tab 2 veces de nuevo 
Specialer$ cd ../../
bin/   home/  lib/   lib64/
Specialer$ cd ../../
bin/   home/  lib/   lib64/
Specialer$


4. Ahora buscar este:  cd ../../home/ y tab 2 veces


5. Ahora se completa asi depues del paso   Specialer$ cd ../../home/ctf-player/  y enter

-Debe estra aqui -pwd
Specialer$ pwd
/home/ctf-player
Specialer$




6.  Ahora: cd ctf-player/ y tab 2 veces
Specialer$ cd ctf-player/
.hushlogin  .profile    abra/       ala/        sim/
Specialer$ cd ctf-player/


Aqui para que funcione se le debe dar tab en esta forma estar amtes de ctf
```

![[Pasted image 20250414221943.png]]


```
7. Entrar a cd cd abra/ -enter


8. echo $(<cadabra.txt)
9.  cd ../ala- Tab 2vcees
10. Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}
Specialer$


Flag: picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}

```





//Referencia
https://josephkimiri.github.io/posts/Specialer/