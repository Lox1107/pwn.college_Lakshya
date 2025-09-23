# Command History
The challenge asks us to check the command history of our terminal to get the flag that was injected in the history.

***

## My solve
**Flag:** `pwn.college{YStDkMuUIytx-MryWgsMsOeJZVP.0lNzEzNxwCNzEzNzEzW}`

I pressed the up arrow :arrow_up: key to check the last command in my command history, i found the flag by pressing it once.

```
hacker@hello~command-history:~$ the flag is pwn.college{YStDkMuUIytx-MryWgsMsOeJZVP.0lNzEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that the shell stores a *history(log)* of previously entered commands which can be accessed by using the up and down arrow keys. These can be really useful if we need to run the same command multiple times in a challenge or use a command we used in a previous challenge again to save us time and remove repetitive typing.

***

## References 
*No references used*