# making directories
The challenge asks us to create a directory at /tmp/pwn, put a file named college inside it, and then run /challenge/run so the checker can verify the task and output the flag.

***

## My solve
**Flag:** `pwn.college{caHJ5EGPoLRyvMqzwkEzKQi0Y5B.QXxMDO0wCNzEzNzEzW}`

I created the /tmp/pwn directory using mkdir, created the college file inside it using touch, and ran /challenge/run to get the flag.
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{caHJ5EGPoLRyvMqzwkEzKQi0Y5B.QXxMDO0wCNzEzNzEzW}
```

***

## What I learned
I learned how to create directories with mkdir and place files in them (for example using touch).
***

## References 
*No references used*