# moving files
The challenge asks us to move the /flag file into /tmp/hack-the-planet using the mv command, then run /challenge/check to verify the move and receive the flag.

***

## My solve
**Flag:** `pwn.college{EHBwKUSGHNSrHIvAmivt4E75Zcv.0VOxEzNxwCNzEzNzEzW}`

I moved the /flag file to /tmp/hack-the-planet using *mv* command and then ran the /challenge/check program to confirm the move and get the flag.
```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{EHBwKUSGHNSrHIvAmivt4E75Zcv.0VOxEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned how to use mv to relocate files within the filesystem by using mv (source /destination), this moves the file and not just copies it.
***

## References 
*No references used*