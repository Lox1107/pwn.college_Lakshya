# Listing Processes
The challenge asks us to find the name of the randomly named /challenge/run program which is already running by using the ps command. Then running it to get the flag.
***

## My solve
**Flag:** `pwn.college{UMnW6j-gdjmXbNqgxwqemhlQ-jb.QX4MDO0wCNzEzNzEzW}`

Since the /challenge directory could not be read with ls but given that the run program was already running, I used the ps -efww command to list all processes, which gave me the randomly named /challenge/29416-run-1456 process, which i then ran to get the flag.
```
hacker@processes~listing-processes:~$ ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 04:11 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 04:11 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 04:11 ?        00:00:00 /challenge/29416-run-1456
root         135     132  0 04:11 ?        00:00:00 sleep 6h
hacker       146       1  0 04:11 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash --login
hacker       150     146  0 04:11 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160     150  0 04:14 pts/0    00:00:00 ps -efww
hacker@processes~listing-processes:~$ /challenge/29416-run-1456
Yahaha, you found me! Here is your flag:
pwn.college{UMnW6j-gdjmXbNqgxwqemhlQ-jb.QX4MDO0wCNzEzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

***

## What I learned
I learned about the ps command which outputs currrently running processes. There are two syntaxes for using the ps command. One is the the standard syntax with -ef argument to list all processes and the BSD syntax with aux argument to list all processes. These two methods show slightly different outputs but both have many similarities too. Also, adding ww to the argument lists the full process names, which may otherwise be truncated since it is limited by the size of the terminal window.
***

## References 
*No references used*