# Redirectign outputs
The challenge asks us to use output redirection so that the text PWN is written to a file named COLLEGE to get the flag.
***

## My solve
**Flag:** `pwn.college{85Z3BzlazOtB9KIImPma0bSBxsZ.QX0YTN0wCNzEzNzEzW}`

i used the echo command to return "PWN" and redirected the output to COLLEGE to get the flag.
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{85Z3BzlazOtB9KIImPma0bSBxsZ.QX0YTN0wCNzEzNzEzW}
```

***

## What I learned
I  learned that we can use > to redirect the output of a command to another file.

***

## References 
*No references used*