## Objetivo
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
You can download the challenge files here:
challenge.zip
ssh -p 65458 ctf-player@atlas.picoctf.net
Using the password 83dcefb7. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!


- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Solución


```
┌──(aratt㉿kali)-[/tmp/tmp.WLxRuf2KIL/home/ctf-player/drop-in]
└─$ ssh -p 65458 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:65458 ([18.217.83.136]:65458)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:65458' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 625
Lower! Try again.
Enter your guess: 570
Higher! Try again.
Enter your guess: 610
Higher! Try again.
Enter your guess: 617
Lower! Try again.
Enter your guess: 613
Lower! Try again.
Enter your guess: 611
Higher! Try again.
Enter your guess: 612
Congratulations! You guessed the correct number: 612
Here's your flag: picoCTF{g00d_gu355_ee8225d0}
Connection to atlas.picoctf.net closed.
                                                                                                                                                                                                                                            
┌──(aratt㉿kali)-[/tmp/tmp.WLxRuf2KIL/home/ctf-player/drop-in]
└─$ 


```
## Notas adicionales

## Referencias 