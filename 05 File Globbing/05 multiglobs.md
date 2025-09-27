# Multiple globs
The challenge asks us to change our cursent working directory into /challenge/files, then run /challenge/run with a single short (≤3 characters) globbed word that has two * wildcards and matches all files containing p.

***

## My solve
**Flag:** `pwn.college{kdwmSmW7C0l1R6aZ7wY8KKg4O62.0lM3kjNxwCNzEzNzEzW}`

I changed into the /challenge/files directory using globs and ran the /challenge/run program with a single argument containing two * globs (*p*), which expanded to every file containing p.
```
hacker@globbing~multiple-globs:~$ cd /ch*/fi*
hacker@globbing~multiple-globs:/challenge/files$ ../run *p*
You got it! Here is your flag!
pwn.college{kdwmSmW7C0l1R6aZ7wY8KKg4O62.0lM3kjNxwCNzEzNzEzW}
```

***

## What I learned
I learned that you can put multiple * wildcards in a single word and the shell will expand the word to every filename that matches the overall pattern. For example, *p* becomes a list of all files whose names contain p. This lets you pass many matching files to a command using one short globbed argument.

***

## References 
*No references used*