# Becoming root with su
The challenge asks us to become the root user using the su command. The challenge provides us with the root password required to become the root through the su command and then asks us to read the flag.
***

## My solve
**Flag:** `pwn.college{MGbwC-qBxQSb5jpL7GlChbXhWbW.QX1UDN1wCNzEzNzEzW}`

First I used the su command to become the root user, the shell then asked me for the root password. I typed in the provided password(hack-the-planet) and became the root user. Then i used cat on the flag file which is always stored at /flag in pwn.college challenges as the root has the permission to read the file and got the flag.
```
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{MGbwC-qBxQSb5jpL7GlChbXhWbW.QX1UDN1wCNzEzNzEzW}
```

***

## What I learned
I learned that we can switch users in the shell using the su(substitute user) command. We can start a root shell by running the su command and by entering the correct root password which it prompts us to enter. The root is the system administrator so it has more permissions than other users which is very helpful for hackers.

***

## References 
*No references used*