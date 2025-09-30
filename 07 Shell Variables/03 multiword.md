# Multi-word Variables
The challenge asks us to set the shell variable PWN to the value COLLEGE YEAH to get the flag.
***

## My solve
**Flag:** `pwn.college{c4k8WgDQfrnHwgkkTQ6pYwNtqy7.QXwYTN0wCNzEzNzEzW}`

I set the variable PWN to the multi‑word value COLLEGE YEAH by pputting quotes around it(i.e. "COLLEGE YEAH") so the shell treats it as a single token and the flag was printed to the terminal.
```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{c4k8WgDQfrnHwgkkTQ6pYwNtqy7.QXwYTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that the shell interprets spaces as separators between commands and arguments, so to assign a multi word value, we have to put quotes around the value so that it is handled like a single token.

***

## References 
*No references used*