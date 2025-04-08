## So Meta
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).

Hinst:
1. What does meta mean in the context of files?
2. Ever heard of metadata?

## Solución

```
 sudo apt install eog
W: Not using locking for read only lock file /var/lib/dpkg/lock-frontend
W: Not using locking for read only lock file /var/lib/dpkg/lock
E: dpkg was interrupted, you must manually run 'sudo dpkg --configure -a' to correct the problem.


someta
wget link
ls pico_img.png
file pico_img.png
strings -n18 pico_img.png   --Se sabe d e donde viene
--Metadadtso de un rchovo o video-aplicacion sudo apt install exiftool(Metadatos- cuando se creo caundo se modifico
)

exiftool pico_img.png

primero los string
Despues los metadatos

exiftool pico_img.png -Artist -Filtrer






Primera Parte:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/meta$ wget https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
--2025-04-08 12:53:49--  https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: ‘pico_img.png’

pico_img.png                  100%[=================================================>] 106.25K   651KB/s    in 0.2s

2025-04-08 12:53:50 (651 KB/s) - ‘pico_img.png’ saved [108795/108795]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/meta$





Segunad Parte:
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/meta$ strings -n18 pico_img.png
"iTXtXML:com.adobe.xmp
" id="W5M0MpCehiHzreSzNTczkc9d"?> <x:xmpmeta xmlns:x="adobe:ns:meta/" x:xmptk="Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27        "> <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"> <rdf:Description rdf:about="" xmlns:xmp="http://ns.adobe.com/xap/1.0/" xmlns:xmpMM="http://ns.adobe.com/xap/1.0/mm/" xmlns:stRef="http://ns.adobe.com/xap/1.0/sType/ResourceRef#" xmp:CreatorTool="Adobe Photoshop CS6 (Windows)" xmpMM:InstanceID="xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B" xmpMM:DocumentID="xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B"> <xmpMM:DerivedFrom stRef:instanceID="xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B" stRef:documentID="xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B"/> </rdf:Description> </rdf:RDF> </x:xmpmeta> <?xpacket end="r"?>
picoCTF{s0_m3ta_d8944929}K





Flag:picoCTF{s0_m3ta_d8944929}





**Segunda Solución** 
-Usando: exiftool

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/foren/meta$ exiftool pico_img.png -Artist -Filtrer
Artist                          : picoCTF{s0_m3ta_d8944929}



```