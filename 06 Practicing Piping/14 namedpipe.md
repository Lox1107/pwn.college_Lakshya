# Named pipes
The challenge asks us to create a FIFO at /tmp/flag_fifo and redirect the stdout of /challenge/run into that FIFO and read in another terminal to get the flag.
***

## My solve
**Flag:** `pwn.college{ACXjc7RmDyIZvDb-77JjNlXg8C3.01MzMDOxwCNzEzNzEzW}`

I created the /tmp/flag_fifo FIFO and redirected /challenge/run’s stdout to it in one terminal, then read from it using cat in another terminal to get the flag.

In 1st terminal:
```
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
```

In 2nd terminal:
```
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{ACXjc7RmDyIZvDb-77JjNlXg8C3.01MzMDOxwCNzEzNzEzW}
```

***

## What I learned
I  learned how to create named pipes(FIFOS) using the mkfifo command and that when writing to it, the writer get blocked until a reader is used to open the FIFO and vice versa.

***

## References 
*No references used*