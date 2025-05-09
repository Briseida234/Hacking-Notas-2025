
## Disk, disk, sleuth!
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/2f998eee12730cf5766624681212a441/dds1-alpine.flag.img.gz)

### Hints:
1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!



## Solución:
```

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/disk$ wget https://mercury.picoctf.net/static/2f998eee12730cf5766624681212a441/dds1-alpine.flag.img.gz
--2025-05-07 22:57:42--  https://mercury.picoctf.net/static/2f998eee12730cf5766624681212a441/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768911 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz       100%[=================================================>]  28.39M  6.54MB/s    in 4.3s

2025-05-07 22:57:47 (6.54 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768911/29768911]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/disk$ gunzip dds1-alpine.flag.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/disk$ srch_strings dds1-alpine.flag.img | grep picoCTF
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/disk$

```


### Bandera
```
picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}
```