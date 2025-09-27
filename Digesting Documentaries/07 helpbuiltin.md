# Help for Builtins
The challenge asks us to use the shell's builtin help to read the documentation for a builtin command named challenge and learn the secret option and value to pass to it so it will print the flag.

***

## My solve
**Flag:** `pwn.college{UNzYzBG6LBSEkRW0-wPiPK_JYbV.QX0ETO0wCNzEzNzEzW}`

I used the help builtin to read the challenge builtin's help text, discovered the secret option(--secret SECRET) and the secret value to be input as argument for the option(UNzYzBG6), and then invoked the builtin with that option and value to get the flag.
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "UNzYzBG6".
hacker@man~help-for-builtins:~$ challenge --secret UNzYzBG6
Correct! Here is your flag!
pwn.college{UNzYzBG6LBSEkRW0-wPiPK_JYbV.QX0ETO0wCNzEzNzEzW}
```

***

## What I learned
i learned that some commands are built into the shell itself (builtins) and you use help <name> to see their documentation.
***

## References 
*No references used*