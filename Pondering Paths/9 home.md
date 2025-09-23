# home sweet home
The challenge asks us to run the /challenge/run program and have it write the flag to a file inside our home directory. The program requires an absolute path as an argument, and the path must be three characters or less before expansion. The home directory can be referenced using ~, which expands to /home/hacker.

***

## My solve
**Flag:** `pwn.college{00c2Zbj3LsLrQd_s37Hn2f4e5EP.QXzMDO0wCNzEzNzEzW}`

I invoked the /challenge/run program and provided a path inside my home directory as an argument. Using the path ~/f met the requirement for a three-character path before expansion and pointed to an absolute path in my home directory. The program wrote the flag to that file and returned it.

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{00c2Zbj3LsLrQd_s37Hn2f4e5EP.QXzMDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that the ~ symbol is short for the current user’s home directory (/home/hacker in this case) and is expanded to an absolute path by the shell. Programs that require an absolute path as an argument can accept paths starting with ~, and the shell will handle the expansion. Also only the leading ~ is expanded(i.e ~/~ corresponds to /home/hacker/~ and not /home/hacker/home/hacker).

***

## References 
*No references used*