# removing files
The challenge asks us to remove a specific file (~/delete_me) using the rm command, then run /challenge/check which will verify whether the file is deleted and print the flag accordingly.

***

## My solve
**Flag:** `pwn.college{cCxJ1-JSpCHS4aDoIRLrmI8smtF.QX2kDM1wCNzEzNzEzW}`

I deleted the delete_me file from my home directory with *rm* and then ran the /challenge/check program to confirm the removal and get the flag.
```
hacker@commands~removing-files:~$ rm ~/delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{cCxJ1-JSpCHS4aDoIRLrmI8smtF.QX2kDM1wCNzEzNzEzW}
```

***

## What I learned
I learned how to remove files with the rm command, where we can remove a file by inputting its path as a argument for the rm command as long as we have the necessary permissions.
***

## References 
*No references used*