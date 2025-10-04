# Using sudo
The challenge gives the hacker(us) user sudo priviliges and asks us to used sudo to read the flag as the root user.
***

## My solve
**Flag:** `pwn.college{c4goIOHnU9miDSeJhPnB8IcL8uY.QX4UDN1wCNzEzNzEzW}`

I used sudo to elevate my priviliges and run the cat command as the root user aand read the /flag file where the flag is stored.
```
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{c4goIOHnU9miDSeJhPnB8IcL8uY.QX4UDN1wCNzEzNzEzW}
```

***

## What I learned
I  learned that su is not used nowadays because it requires root passwords, which can be leaked, so intead we use sudo. The list of users that can use sudo is stored in the /etc/sudoers file. sudo essentially allows us to run a command as the root user without running a separate root shell.

***

## References 
*No references used*