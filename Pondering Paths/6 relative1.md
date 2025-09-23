# implicit relative paths, from /
The challenge asks us to run the /challenge/run program using a relative path while the current working directory is /(i.e. just challenge/run) to get the flag.

***

## My solve
**Flag:** `pwn.college{EXlo9PUXGx0C7fc9yy6ykAcX2Jf.QX5QTN0wCNzEzNzEzW}`

I changed my current working directory to / and then invoked the challenge/run program using a relative path (no leading /) to get the flag.

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EXlo9PUXGx0C7fc9yy6ykAcX2Jf.QX5QTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that a relative path does not start with / and is interpreted relative to the shell’s current working directory. Changing the current working directory with cd affects how relative paths are interpreted, so when using a relative path, it is important to position yourself in the correct directory to ensure proper output.

***

## References 
*No references used*