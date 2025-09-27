# Mixing globs
The challenge asks us to change into /challenge/files and, using a single short glob (6 characters or less) that should combine the glob types you’ve learned, pass one argument to /challenge/run that matches the filenames challenging, educational, and pwning.

***

## My solve
**Flag:** `pwn.college{cp6QTM3UR6LbWMWJuKYeTM5YGLe.QX1IDO0wCNzEzNzEzW}`

I changed into the /challenge/files directory and listed all files. I noticed that no other words started with the initial letters of the target arguments so I used a bracket glob that matches the initial letters of the three target words and a trailing * to match the rest and got the flag.
```
hacker@globbing~mixing-globs:~$ cd /ch*/fi*
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~mixing-globs:/challenge/files$ ../run [cep]*
You got it! Here is your flag!
pwn.college{cp6QTM3UR6LbWMWJuKYeTM5YGLe.QX1IDO0wCNzEzNzEzW}
```

***

## What I learned
I learned how to combine bracket globs with * wildcard so one short pattern can match multiple specific filenames. Eg:[cep]* matches any filename starting with c, e, or p, followed by anything.

***

## References 
*No references used*