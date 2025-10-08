# Killing Processes
The challenge asks us to kill the currently running /challenge/dont_run process to in turn run the /challenge/run program which cannot be run if dont_run is already running to get the flag.
***

## My solve
**Flag:** `pwn.college{MnKRKAOyiqmVjZTYBITdv-wDYNm.QXyQDO0wCNzEzNzEzW}`

First I used ps -ef to list all running commands and redirected its output to grep with the search term /challenge/dont_run to find the process ID(136) of the unwanted process. Then I used the kill command with 136 as the argument to kill the dont_run process. Finally I ran /challenge/run after killing the dont_run process to get the flag.
```
hacker@processes~killing-processes:~$ ps -ef | grep /challenge/dont_run
hacker       136     135  0 04:34 ?        00:00:00 /challenge/dont_run
hacker       165     152  0 04:36 pts/0    00:00:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{MnKRKAOyiqmVjZTYBITdv-wDYNm.QXyQDO0wCNzEzNzEzW}
```

***

## What I learned
I learned about the kill command which can be used to terminate running processes by passing their process ID as an argument to kill(i.e kill <PID>). 

***

## References 
*No references used*