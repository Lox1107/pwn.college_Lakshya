# Exporting Variables
The challenge asks us to run /challenge/run with the variable PWN set to value COLLEGE and exported and the variable COLLEGE set to value PWN but not exported to hget the flag.
***

## My solve
**Flag:** `pwn.college{I_l10QSTED4PjhZWX_VgeEJ02vo.QXyYTN0wCNzEzNzEzW}`

I exported variable PWN with the value COLLEGE so it is inherited by /challenge/run, and I set COLLEGE to PWN without exporting it so it remained local to parent shell. Then, I ran the /challenge/run command to get the flag.
```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{I_l10QSTED4PjhZWX_VgeEJ02vo.QXyYTN0wCNzEzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

***

## What I learned
I learned that if we just set a variable normally, it only exists in our current shell and child processes cannot see it. But if we use export, the variable is also shared with child processes.

***

## References 
*No references used*