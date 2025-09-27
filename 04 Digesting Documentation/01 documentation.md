# Learning from Documentation
The challenge asks us to run /challenge/challenge with the correct argument as specified by its documentation: pass the --giveflag argument so the program outputs the flag.

***

## My solve
**Flag:** `pwn.college{Q2iAlmCR4zDEaH1g6f1GrcdZ0eL.QX0ITO0wCNzEzNzEzW}`

I invoked the challenge program with the documented argument --giveflag and it printed the flag.
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{Q2iAlmCR4zDEaH1g6f1GrcdZ0eL.QX0ITO0wCNzEzNzEzW}
```

***

## What I learned
Programs expect specific arguments to change their behavior. Reading documentation(basically a guidebook) tells you which arguments to use. In this case the doc said to use --giveflag, so running /challenge/challenge --giveflag made the program print the flag.
***

## References 
*No references used*