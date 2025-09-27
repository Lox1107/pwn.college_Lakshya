# explicit relative paths, from /
The challenge asks us to run the /challenge/run program using a relative path that explicitly includes . to refer to the current directory to get the flag.

***

## My solve
**Flag:** `pwn.college{8z4jcEXF5cYjuf5LldkxdYSM8WC.QXwUTN0wCNzEzNzEzW}`

I changed my current working directory to / and then invoked the challenge/run program using the relative path ./challenge/run to get the flag where . refers to the same current directory.

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8z4jcEXF5cYjuf5LldkxdYSM8WC.QXwUTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that the . in a path refers to the current directory, so adding . explicitly in a relative path does not change which file is accessed. Using ./challenge/run is equivalent to challenge/run when the current working directory is /.

***

## References 
*No references used*