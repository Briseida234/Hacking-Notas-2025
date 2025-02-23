## Binary search

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/6/challenge.zip)

`ssh -p 57721 ctf-player@atlas.picoctf.net`Using the password `6dd28e9b`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!



Hints:
1. ¿Alguna vez has jugado a la búsqueda fría o caliente? La búsqueda binaria es un poco así.
2. Tienes un número muy limitado de posibilidades. ¡Prueba a hacer saltos más grandes entre números!
3. El programa elegirá aleatoriamente un nuevo número cada vez que te conectes. Siempre puedes volver a intentarlo, pero deberías comenzar tu búsqueda binaria desde el principio: prueba con alrededor de 500. ¿Se te ocurre por qué?



## Solución:

```
grbau21-picoctf@webshell:~$ ssh -p 57721 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 300
Lower! Try again.
Enter your guess: 100
Lower! Try again.
Enter your guess: 50
Lower! Try again.
Enter your guess: 30
Lower! Try again.
Enter your guess: 10
Lower! Try again.
Enter your guess: 5
Lower! Try again.
Enter your guess: 1
Congratulations! You guessed the correct number: 1
Here's your flag: picoCTF{g00d_gu355_de9570b0}
Connection to atlas.picoctf.net closed.
grbau21-picoctf@webshell:~$ 
```
