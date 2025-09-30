# Setting Variables
The challenge asks us to set the shell variable PWN to the value COLLEGE to get the flag.
***

## My solve
**Flag:** `pwn.college{YQsSDp0HJ0Ija64I975eris2zUW.QX5UTN0wCNzEzNzEzW}`

I assigned COLLEGE to the variable PWN and the flag was printed to the terminal.
```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YQsSDp0HJ0Ija64I975eris2zUW.QX5UTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that we can set shell variables with NAME=value (without using spaces). We can use NAME to set variables and $NAME to read them. Also, variable names and values are case‑sensitive.

***

## References 
*No references used*