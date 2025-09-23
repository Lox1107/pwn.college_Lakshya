# The Root
The challenge asks us to run the pwn program from its absolute path(which is the root(/) path)

***

## My solve
**Flag:** `pwn.college{EmEmtcNCRxr7J-gOLe3ZvVkvh8M.QX4cTO0wCNzEzNzEzW}`

I invoked the /pwn program to get the flag.
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{EmEmtcNCRxr7J-gOLe3ZvVkvh8M.QX4cTO0wCNzEzNzEzW}
```

***

## What I learned
I learnt that the filesystme starts at the *root(/)* directory and that we can add programs in a directory(pwn was added to /). We can invoke a program by entering its path on the command line(pwn can be invoked by entering /pwn), this path which starts with the root(/) directory, is called an 'absolute path'.

***

## References 
*No references used*