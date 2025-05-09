
## Operation Oni
Descargue esta imagen de disco, busque la clave e inicie sesión en la máquina remota.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.

- [Descargar imagen de disco](https://artifacts.picoctf.net/c/71/disk.img.gz)
- Máquina remota:`ssh -i key_file -p 62580 ctf-player@saturn.picoctf.net`


### Hints:
1. (None)


## Solución:

```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ wget https://artifacts.picoctf.net/c/71/disk.img.gz
--2025-05-07 22:39:24--  https://artifacts.picoctf.net/c/71/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 48132743 (46M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                                 0%[                                                                         disk.img.gz                                 0%[                                                                         disk.img.gz                                 0%[                                                                         disk.img.gz                   100%[=================================================>]  45.90M  2.64MB/s    in 15s

2025-05-07 22:39:41 (3.14 MB/s) - ‘disk.img.gz’ saved [48132743/48132743]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ gzip -d disk.flag.img.gz
gzip: disk.flag.img.gz: No such file or directory
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ gzip -d disk.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ mmls disk.img.gz
Error stat(ing) image file (raw_open: image "disk.img.gz" - No such file or directory)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ ls
disk.img
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ fls disk.img -o 206848
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ fls disk.img -o 206848 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ fls disk.img -o 206848 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ icat disk.img -o 206848 2345
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ icat disk.img -o 206848 2345 > key_file
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ chmod 600 key_file
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/operoni$ ssh -i key_file -p 62580 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:62580 ([13.59.203.175]:62580)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:8: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:62580' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

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

ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$

```

### Bandera

```
picoCTF{k3y_5l3u7h_af277f77}
```