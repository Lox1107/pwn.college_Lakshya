# Helpful Programs
The challenge asks us to invoke the program with a help-style argument (such as -h or --help) to discover how to use it. And from the help command output, find the correct arguments to get the flag.

***

## My solve
**Flag:** `pwn.college{UUOEhIPxJPVVJ2w2zpRWI_8zsGK.QX3IDO0wCNzEzNzEzW}`

I ran the /challenge/challenge program’s help to discover the correct options, used -p to reveal the secret value to be used in -g(228), then passed that value to the -g option while running /challenge/challenge to get the flag.
```
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 228
hacker@man~helpful-programs:~$ /challenge/challenge -g 228
Correct usage! Your flag: pwn.college{UUOEhIPxJPVVJ2w2zpRWI_8zsGK.QX3IDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that many programs print a short usage message if you run them with -h or --help. That usage message shows the available options and how to pass values to them.
***

## References 
*No references used*