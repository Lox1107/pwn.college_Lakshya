# Process substitution for input
The challenge asks us to pipe the output of /challenge/pwn to /challenge/college but we need to intercept it using the **tee** command while passing the value to understand what argument /challenge/pwn needs to be run with so that the input going into /challenge/college is correct to get the flag.
***

## My solve
**Flag:** `pwn.college{kLvjN9W76gnbWORTqzQuwiekIsW.QXxITO0wCNzEzNzEzW}`

I used the tee command to intercept the output of /challenge/pwn and save it to a file named /intercept. Then I read the /intercept file to find the secret argument. Then I re-ran /challenge/pwn with the --secret argument and value(kLvjN9W7) which i found by readin the intercepted output and piped that to /challenge/college to get the flag.
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee /intercept | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat intercept
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "kLvjN9W7"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret kLvjN9W7 | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{kLvjN9W76gnbWORTqzQuwiekIsW.QXxITO0wCNzEzNzEzW}
```

***

## What I learned
I learned that the tee command can be used to duplicate the output of a command by copying whatever is entered into a pipe to a file and another commad together. This is useful when we need to pass the same output to multiple programs or intercept the output of the first program.

***

## References 
*No references used*