# Writing to multiple programs
The challenge asks us to run /challenge/hack and duplicate its output so that it becomes the input to both /challenge/the and /challenge/planet to get the flag.
***

## My solve
**Flag:** `pwn.college{U-XNN3mmsJ85dBzQAsSCtM5OrNE.QXwgDN1wCNzEzNzEzW}`

I used the tee command along with process substitution to send the output of /challenge/hack into both /challenge/the and /challenge/world to get the flag.
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{U-XNN3mmsJ85dBzQAsSCtM5OrNE.QXwgDN1wCNzEzNzEzW}
```

***

## What I learned
I learned that >(command) makes the shell treat a command just like a file, so tee >(command) can be used to write a single output into the input of multiple commands.

***

## References 
*No references used*