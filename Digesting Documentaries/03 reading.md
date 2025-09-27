# Reading Manuals
The challenge asks us to read the manual page for the challenge program (via man challenge) to discover a secret command option that causes the program to print the flag.

***

## My solve
**Flag:** `pwn.college{4kr5GpzsoP8GuZ8sfOZONzvXkhA.QX0EDO0wCNzEzNzEzW}`

I read the challenge manpage to learn the secret option krpzso, then ran the program with that option and the argument as 458 to get the flag.
```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --krpzso 458
Correct usage! Your flag: pwn.college{4kr5GpzsoP8GuZ8sfOZONzvXkhA.QX0EDO0wCNzEzNzEzW}
```

***

## What I learned
Manpages (viewed with man <command>) document how programs are used and list options and arguments. When a program has an undocumented option, we can look at its manpage for help.
***

## References 
*No references used*