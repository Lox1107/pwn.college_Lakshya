# cat: not the pet, the command!
The challenge asks us to read the flag file that is stored in our home directory using the *cat* command.

***

## My solve
**Flag:** `pwn.college{UsfagI09oke8rFqTI6ASLfDKu3P.QXxcTN0wCNzEzNzEzW}`

I used the cat command on the flag file stored in my home directory(i.e cat flag) to get the flag.
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{UsfagI09oke8rFqTI6ASLfDKu3P.QXxcTN0wCNzEzNzEzW}
```

***

## What I learned
I learned that cat prints the contents of files to standard output and can concatenate multiple files if multiple arguments are passed. If no arguments are provided,  cat reads from the terminal input and outputs it.

***

## References 
*No references used*