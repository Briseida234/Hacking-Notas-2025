
### Sleuthkit Apprentice
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)


#### Hints:
1. (None)


## Solución:

```
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz
--2025-05-07 12:55:31--  https://artifacts.picoctf.net/c/137/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534568 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz     100%[=====================>]  45.33M  13.2MB/s    in 6.7s

2025-05-07 12:55:38 (6.73 MB/s) - ‘disk.flag.img.gz’ saved [47534568/47534568]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ ls -la disk.flag.img.gz
-rw-r--r-- 1 brisguz brisguz 47534568 Mar 15  2023 disk.flag.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ gzip -d disk.flag.img.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ ls -lah disk.flag.img
-rw-r--r-- 1 brisguz brisguz 300M Mar 15  2023 disk.flag.img
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img - o 360448
Error stat(ing) image file (raw_open: image "-" - No such file or directory)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 360448
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
d/d 1986:       proc
d/d 1987:       dev
d/d 1988:       tmp
d/d 1989:       lib
d/d 1990:       var
d/d 3969:       usr
d/d 3970:       bin
d/d 1991:       sbin
d/d 1992:       media
d/d 1993:       mnt
d/d 1994:       opt
d/d 1995:       root
d/d 1996:       run
d/d 1997:       srv
d/d 1998:       sys
d/d 2358:       swap
V/V 31745:      $OrphanFiles
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 206848
Cannot determine file system type
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 206848 -r
Cannot determine file system type
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 360448 -r




2. Último
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 360448 1995
r/r 2363:       .ash_history
d/d 3981:       my_folder
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 360448 3981
r/r * 2082(realloc):    flag.txt
r/r 2371:       flag.uni.txt
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ fls disk.flag.img -o 360448 2371
Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 2371
)
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$ icat disk.flag.img -o 360448 2371
picoCTF{by73_5urf3r_adac6cb4}
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/for4/sleapp$

```

### Bandera

```

picoCTF{by73_5urf3r_adac6cb4}

```