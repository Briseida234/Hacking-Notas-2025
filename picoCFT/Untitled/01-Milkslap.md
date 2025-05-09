
### Milkslap
http://mercury.picoctf.net:7585/



Hints:
1. Look at the problem category



## Solución:
```
1. Descragar la imagen con el nombre
2. Primer ver codigo fuente
3. Entar a styless
4. Nombre de la imagen (concat_v.png)
5. Descargar ahora si la imagen y guardar


6. gem install zteg
brisguz@DESKTOP-8V24E1B:/$ sudo gem install zsteg
Fetching iostruct-0.5.0.gem
Fetching rainbow-3.1.1.gem
Fetching zpng-0.4.5.gem
Fetching zsteg-0.2.13.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.5.0
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.5.0
Installing ri documentation for iostruct-0.5.0
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 4 seconds
4 gems installed
brisguz@DESKTOP-8V24E1B:/$




7. export RUBY_THREAD_VM_STACK_SIZE=500000000
8. zsteg concat_v.png
9. Bandera
picoCTF{imag3_m4n1pul4t10n_sl4p5}

```

### Bandera
```

picoCTF{imag3_m4n1pul4t10n_sl4p5}
```






