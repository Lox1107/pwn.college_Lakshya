# Tab completion on commands
The challenge asks us to use the shell's tab completion for commands: start typing the command prefix pwncollege and press Tab to auto-complete the full command and run it to get the flag.

***

## My solve
**Flag:** `pwn.college{YfC8VQKBE8zpjasS-Sa8z_m5cg7.0VN0EzNxwCNzEzNzEzW}`

I typed the pwncollege prefix and used the shell's tab completion to expand it to the full command (pwncollege-27838), then executed it to get the flag.
```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-27838 
Correct! Here is your flag:
pwn.college{YfC8VQKBE8zpjasS-Sa8z_m5cg7.0VN0EzNxwCNzEzNzEzW}
```

***

## What I learned
I  learned that tab completion works for commands as well as filenames. Typing part of a command and pressing Tab lets the shell complete available command names, which saves typing and prevents mistakes, but always check the completed text before hitting Enter so we don't accidentally run the wrong command.

***

## References 
*No references used*