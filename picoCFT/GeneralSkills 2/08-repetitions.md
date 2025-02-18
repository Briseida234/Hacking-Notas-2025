## Repetitions
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/472/enc_flag).


Hints:
Multiple decoding is always good.

## Solución 1:

*  Usando Cyberchef
```
Input: VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKeldWaHdRMDB4V2tWU2JFNVdDbUpXV2tkVU1WcFhWVzFHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==


Recipe: 
From Base64
From Base64
From Base64
From Base64
From Base64
From Base64

Outpout:
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190}
```





## Solución 2 :
```
grbau21-picoctf@webshell:~$ cat enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKeldWaHdRMDB4V2tWU2JFNVdDbUpXV2tkVU1WcFhWVzFHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
grbau21-picoctf@webshell:~$ cat enc_flag | base64 -d| base64 -d| base64 -d| base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
ek0wT1RReE9UQjlDZz09Cg==
grbau21-picoctf@webshell:~$ cat enc_flag | base64 -d| base64 -d| base64 -d| base64 -d^C
grbau21-picoctf@webshell:~$ cat enc_flag | base64 -d| base64 -d| base64 -d| base64 -d| base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNzM0OTQxOTB9Cg==

grbau21-picoctf@webshell:~$ cat enc_flag | base64 -d| base64 -d| base64 -d| base64 -d| base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190}
grbau21-picoctf@webshell:~$ 
```