# Redirecting inputs
The challenge asks us to run /challenge/run with its standard input redirected from a file named PWN and the PWN file must contain the text COLLEGE to get the flag.
***

## My solve
**Flag:** `pwn.college{oqc4LGsr1J-2t66tWfigXtytk0C.QXwcTN0wCNzEzNzEzW}`

I redirected COLLEGE into the file PWN and then redirected the PWN file into /challenge/run's stdin to get the flag.
```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{oqc4LGsr1J-2t66tWfigXtytk0C.QXwcTN0wCNzEzNzEzW}
```

***

## What I learned
I  learned that < redirects a file into a program’s standard input.

***

## References 
*No references used*