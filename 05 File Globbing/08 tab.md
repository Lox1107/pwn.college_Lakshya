# Tab completion
The challenge asks us to read the file /challenge/pwncollege, but we must use the shell's tab completion (pressing Tab) to expand the name instead of typing it out manually. Once the filename has been completed by the shell, we can cat it to get the flag.

***

## My solve
**Flag:** `pwn.college{YkRt4kuu1RuBDsyZ9RVepoewcl1.0FN0EzNxwCNzEzNzEzW}`

I used tab completion to expand the hidden filename and then used cat on the completed path to read the flag.
```
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ 
pwn.college{YkRt4kuu1RuBDsyZ9RVepoewcl1.0FN0EzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that tab completion lets the shell fill in filenames (or other tokens) for us so we don't have to type the whole name and to avoid mistakes. If a filename is tricky or contains hidden characters, pressing Tab will expand it to the exact name the shell sees, and then we can run commands like cat on the completed path.

***

## References 
*No references used*