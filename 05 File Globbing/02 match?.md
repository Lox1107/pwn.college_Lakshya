# Matching with ?
The challenge asks us to change directory into /challenge using the single-character wildcard ? (so each ? matches exactly one character). After using a ?-based glob to cd into the challenge directory while replacing 'c' and 'l' by ?, run the /challenge/run program from there to get the flag.

***

## My solve
**Flag:** `pwn.college{MSnvdqM2qWgsvOmwomhkU9SWEt-.QXyIDO0wCNzEzNzEzW}`

I used a ? pattern to match the missing characters 'c' and 'l' in /challenge, changed into that directory, and ran the run program to get the flag.
```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MSnvdqM2qWgsvOmwomhkU9SWEt-.QXyIDO0wCNzEzNzEzW}
```

***

## What I learned
The ? wildcard matches exactly one character. By placing ? characters where letters were missing, the shell expanded /?ha??enge into /challenge, letting me cd there without typing every letter. Globs like ? are useful when you know the length and rough shape of a filename or directory but not every character.

***

## References 
*No references used*