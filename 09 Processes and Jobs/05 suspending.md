# Redirectign outputs
The challenge asks us to run the run program and suspend it, then run another instance the run program to get the flag since it only prints the output if there are multiple instances of the run process currently running.
***

## My solve
**Flag:** `pwn.college{Y80qhfCX173D9NNrIYpZlx5xrvZ.QX1QDO0wCNzEzNzEzW}`

First I ran the /challenge/run program but it did not print the flag since it was the only instance of run, then used Ctrl-Z to suspend the progress and keep it in the background. Then I ran another instance of /challenge/run which then checked for other instances of it and printed the flag after finding the background process.
```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 05:18 pts/0    00:00:00 bash /challenge/run
root         148     146  0 05:18 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 05:18 pts/0    00:00:00 bash /challenge/run
root         153     136  0 05:18 pts/0    00:00:00 bash /challenge/run
root         155     153  0 05:18 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{Y80qhfCX173D9NNrIYpZlx5xrvZ.QX1QDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that we can suspend processes running in the terminal using the hotkey Ctrl+Z.

***

## References 
*No references used*