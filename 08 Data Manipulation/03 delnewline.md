# Deleting newlines 
The challenge injects line breaks into the output flag of /challenge/run and asks us to delete all these newlines using tr -d to get the flag.
***

## My solve
**Flag:** `pwn.college{Epbb4y86kNdl2vWA-fiw8CqWIXd.0VNxEzNxwCNzEzNzEzW}`

First I ran the /challenge/run program but the flag was printed across many lines. I then piped that flag through the tr command while using the -d(delete) argument and deleted all the line breaks(i.e. tr -d "\n") to get the flag.
```
hacker@data~deleting-newlines:~$ /challenge/run
Your line-split flag: 
p
wn.
co
l
leg
e
{E
p
b
b
4
y
86kN
dl2v
W
A-
f
iw8
C
qW
I
X
d.
0V
N
x
EzNx
w
CN
zEz
Nz
E
z
W
}

hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{Epbb4y86kNdl2vWA-fiw8CqWIXd.0VNxEzNxwCNzEzNzEzW}
```

***

## What I learned
I  learned that we can use escape sequences to refer to some data that is tough to enter into the terminal. For example we cannot normally enter a newline to the terminal because pressing enter runs the command, but we can use "\n" where \ is called the escape character to represent a newline. the escape sequence must be in quotes to prevent the shell from interpreting it as a separate parameter.

***

## References 
*No references used*