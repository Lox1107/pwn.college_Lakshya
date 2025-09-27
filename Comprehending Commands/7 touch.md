# touching files
The challenge asks us to create two empty files at /tmp/pwn and /tmp/college using the touch command, then run /challenge/run to get the flag.

***

## My solve
**Flag:** `pwn.college{8uBzJogEVpi7-3tFOndt2-m8d1C.QXwMDO0wCNzEzNzEzW}`

I created the required files(/tmp/pwn and /tmp/college) using *touch* and then executed /challenge/run to get the flag.
```
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{8uBzJogEVpi7-3tFOndt2-m8d1C.QXwMDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that the touch command creates files at the specified location given as a parameter, which is a quick way to make empty files.
***

## References 
*No references used*