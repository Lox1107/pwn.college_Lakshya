# Searching Manuals
The challenge asks us to read the challenge program's man page and use the manpage viewer's search features to discover the option that prints the flag.

***

## My solve
**Flag:** `pwn.college{o7Xtjqoa5fgdjpZ3UJWF-iW_Fw9.QX1EDO0wCNzEzNzEzW}`

I opened the manual for challenge and then used ? to search for the keyword *flag* and found the hidden option --saxzw which on pasing as argument to /challenge/challenge gave me the flag.
```
hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ /challenge/challenge --saxzw
Initializing...
Correct usage! Your flag: pwn.college{o7Xtjqoa5fgdjpZ3UJWF-iW_Fw9.QX1EDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that manpages can be navigated with the up/down arrow keys and the PgUp/PgDn keys and that the manpage viewer lets you search inside the page (with / and ?, and navigate the matches with n/N).
***

## References 
*No references used*