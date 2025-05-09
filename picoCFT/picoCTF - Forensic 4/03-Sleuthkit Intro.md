

### Sleuthkit Intro
```

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 64804`

#### Hints:
1. (None)


## Solución:

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2025-05-07 12:48:36--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz          100%[=====================>]  28.34M  17.6MB/s    in 1.6s

2025-05-07 12:48:38 (17.6 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ ls -la disk.img.gz
-rw-r--r-- 1 brisguz brisguz 29714372 Aug  4  2023 disk.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ gzip -d disk.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ ls -la disk.img.gz
ls: cannot access 'disk.img.gz': No such file or directory
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ ls -la disk.img
-rw-r--r-- 1 brisguz brisguz 104857600 Aug  4  2023 disk.img



Ingresar el comando y después poner esto al conectarse 202752, que viene en la parte de ahí:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/intro$ nc saturn.picoctf.net 64804
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```

### Bandera

```
picoCTF{mm15_f7w!}

```