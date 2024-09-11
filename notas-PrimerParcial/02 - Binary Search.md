# Retos PicoCTF


## Objetivo 

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/19/challenge.zip)

Additional details will be available after launching your challenge instance.
## Solución 

```
jesus@jesus-ThinkPad-T420:/$ ssh -p 52098 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:52098 ([18.217.83.136]:52098)' can't be established.
ECDSA key fingerprint is SHA256:ordTMCwK3qpNza5KnIvhhv3zuT2jVOfUn+VlRwYK23s.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:52098,[18.217.83.136]:52098' (ECDSA) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 300
Lower! Try again.
Enter your guess: 200
Higher! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 280
Congratulations! You guessed the correct number: 280
Here's your flag: picoCTF{g00d_gu355_1597707f}
Connection to atlas.picoctf.net closed.
jesus@jesus-ThinkPad-T420:/$ 
```

## Notas adicionales 
Adivinar el numero deacuerdo a las pistas 
## Referencias 
