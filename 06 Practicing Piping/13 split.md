# Split-piping stderr and stdout
The challenge asks us to run /challenge/hack and pipe its stdout into /challenge/planet while sending its stderr into /challenge/the to get the flag.
***

## My solve
**Flag:** `pwn.college{oq1SHyf_HbOp9eZFknuZ2g5ubRm.QXxQDM2wCNzEzNzEzW}`

I used output process substitution for both streams, stdout and stderr, so they were routed to the two target programs separately.
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{oq1SHyf_HbOp9eZFknuZ2g5ubRm.QXxQDM2wCNzEzNzEzW}
```

***

## What I learned
I  learned that we can route stdout and stderr to different commands by using output separate process substitution > >(command) for stdout and 2> >(command) for stderr.

***

## References 
*No references used*