# Matching with *
The challenge asks us to use shell globbing (the * wildcard) so that the argument passed to cd is at most four characters long, and still move into the /challenge directory. After changing into /challenge, run the /challenge/run command to get the flag.

***

## My solve
**Flag:** `pwn.college{IHxxwGYYtWp7I6Rl2ssDL86mgvs.QXxIDO0wCNzEzNzEzW}`

I used the * wildcard to expand /ch* into /challenge, changed into that directory, and then ran the run program to get the flag.
```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{IHxxwGYYtWp7I6Rl2ssDL86mgvs.QXxIDO0wCNzEzNzEzW}
```

***

## What I learned
Globs are a handy way to refer to files or directories when you don't want to type the full name. The * wildcard (glob) makes the shell expand a short pattern into matching filenames or directories. 

***

## References 
*No references used*