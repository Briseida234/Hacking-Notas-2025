## Static ain't always noise

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!


Hints:
(None)

## Solución:
```
grbau21-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
--2025-02-17 18:26:51--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                          100%[======================================================================================================>]   8.18K  --.-KB/s    in 0s      

2025-02-17 18:26:51 (231 MB/s) - 'static' saved [8376/8376]

grbau21-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
--2025-02-17 18:27:13--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                        100%[======================================================================================================>]     785  --.-KB/s    in 0s      

2025-02-17 18:27:13 (367 MB/s) - 'ltdis.sh' saved [785/785]

grbau21-picoctf@webshell:~$ chmod +x static
grbau21-picoctf@webshell:~$ ./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
grbau21-picoctf@webshell:~$ file ltdis.sh
ltdis.sh: Bourne-Again shell script, ASCII text executable
grbau21-picoctf@webshell:~$ cat ltdis.sh
#!/bin/bash



echo "Attempting disassembly of $1 ..."


#This usage of "objdump" disassembles all (-D) of the first file given by 
#invoker, but only prints out the ".text" section (-j .text) (only section
#that matters in almost any compiled program...

objdump -Dj .text $1 > $1.ltdis.x86_64.txt


#Check that $1.ltdis.x86_64.txt is non-empty
#Continue if it is, otherwise print error and eject

if [ -s "$1.ltdis.x86_64.txt" ]
then
        echo "Disassembly successful! Available at: $1.ltdis.x86_64.txt"

        echo "Ripping strings from binary with file offsets..."
        strings -a -t x $1 > $1.ltdis.strings.txt
        echo "Any strings found in $1 have been written to $1.ltdis.strings.txt with file offset"



else
        echo "Disassembly failed!"
        echo "Usage: ltdis.sh <program-file>"
        echo "Bye!"
fi
grbau21-picoctf@webshell:~$ bash ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
grbau21-picoctf@webshell:~$ cat static.ltdis.string.txt | grep picoCTF
cat: static.ltdis.string.txt: No such file or directory
grbau21-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_6f8c8200}

```

