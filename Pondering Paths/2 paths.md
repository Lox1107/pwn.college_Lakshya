# Program and absolute paths
The challenge asks us to execute the run program from the challenge directory using its absolute path(/challenge/run) to get the flag

***

## My solve
**Flag:** `pwn.college{UqP7rZ_h59Ph5IfKI6yrcLgjTQl.QX1QTN0wCNzEzNzEzW}`

I invoked the run program using its absolute path /challenge/run to get the flag

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{UqP7rZ_h59Ph5IfKI6yrcLgjTQl.QX1QTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that there can be more complicated paths. In this level the run program is present in the /challenge directory, so its absolute path is /challenge/run. We can execute a program by entering it's absolute path on the command line no matter what our current working directory is.

***

## References 
*No references used*