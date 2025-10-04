# Other users with su
The challenge asks us to switch to the user *zardus* using the su command and gives us the password to zardus. Then it asks us to run the /challenge/run program while being zardus to get the flag.
***

## My solve
**Flag:** `pwn.college{sa0Sl4bkIc1KTTPasn4CctBjunm.QX2UDN1wCNzEzNzEzW}`

i used the echo command to return "PWN" and redirected the output to COLLEGE to get the flag.
```
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{sa0Sl4bkIc1KTTPasn4CctBjunm.QX2UDN1wCNzEzNzEzW}
```

***

## What I learned
I  learned that we can give a username as an argument to the su command to switch to that user as long as we have the password to that users account. Inputting the correct password switches the shell's current user and allows us access to that users permissions, so we can run programs or read files they had access to.

***

## References 
*No references used*