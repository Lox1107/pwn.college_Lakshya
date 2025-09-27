# listing files
The challenge asks us to list the contents of the /challenge directory with ls to discover the randomly renamed /challenge/run program, then execute that file to get the flag.

***

## My solve
**Flag:** `pwn.college{MH96XyF8HNHUzCSNVAM0r4_8Mab.QX4IDO0wCNzEzNzEzW}`

I listed /challenge to find the renamed command and then executed it to get the flag.
```
hacker@commands~listing-files:~$ ls /challenge
15008-renamed-run-2082  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/15008-renamed-run-2082
Yahaha, you found me! Here is your flag:
pwn.college{MH96XyF8HNHUzCSNVAM0r4_8Mab.QX4IDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that ls lists all directory contents and is useful when file names are unknown or random. If we find the target file, we can run it by using its path.
***

## References 
*No references used*