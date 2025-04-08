## Shark On Wire 1

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

Hinst:
1. Try using a tool like Wireshark
2. What are streams?

## Solución
```

picoCTF{StaT31355_636f6e6e}

Se pone buscar: udp.stream eq 0,1 y 6
Después Analizar-Seguir-UDP


Priemra Parte:
Descargar Directamente el archivo
Depues abrir el archivo desde Wireshark
capture.pcap



```


![[Pasted image 20250408134346.png]]



![[Pasted image 20250408134513.png]]



```

Buscar siguiente, en la barra de buscar


```

![[Pasted image 20250408134654.png]]



```
Y la ultima: udp.stream eq 6
flag: picoCTF{StaT31355_636f6e6e}
```

![[Pasted image 20250408134808.png]]