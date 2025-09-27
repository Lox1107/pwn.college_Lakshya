# Exclusionary globbing
The challenge asks us to use an inverted bracket glob to match all files in /challenge/files whose names do not start with p, w, or n, and pass those matches as a single argument to /challenge/run.   

***

## My solve
**Flag:** `pwn.college{El3cPCwfvVIhPR0E4ThhEw1nm1W.QX2IDO0wCNzEzNzEzW}`

I changed into the /challenge/files directory and ran /challenge/run with an inverted bracket glob ([!pwn]*) so the shell expanded the argument to every filename that does not begin with p, w, or n. The program returned the flag.
```
hacker@globbing~exclusionary-globbing:~$ cd /ch*/fi*
hacker@globbing~exclusionary-globbing:/challenge/files$ ../run [!pwn]*
You got it! Here is your flag!
pwn.college{El3cPCwfvVIhPR0E4ThhEw1nm1W.QX2IDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that putting ! (or ^ in some shells) as the first character inside [] in a glob inverts the character set: [!pwn] matches any single character that is not p, w, or n. Combined with * ([!pwn]*) this matches all filenames whose first letter is none of p, w or n

***

## References 
*No references used*