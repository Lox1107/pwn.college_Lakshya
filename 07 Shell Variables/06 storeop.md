# Storing Command Output
The challenge asks us to use command substitution to store the output of /challenge/run in the PWN variable and print the variable to get the flag.
***

## My solve
**Flag:** `pwn.college{cW9LEDn_fWrUGzGkFpjfAG7wxkZ.QX1cDN1wCNzEzNzEzW}`

I used command substitution to store the output of challenge/run in the PWN variable(by running PWN=$(/challenge/run)). Then i printed the PWN variable(echo $PWN) to get the flag.
```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{cW9LEDn_fWrUGzGkFpjfAG7wxkZ.QX1cDN1wCNzEzNzEzW}
```

***

## What I learned
I learned that we can store the output of a command in a variable by using VARNAME=$(command). We can also use VARNAME='command' but () is preffered over ''.

***

## References 
*No references used*