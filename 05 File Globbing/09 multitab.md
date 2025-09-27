# Multiple options for tab completion
The challenge asks us to use the shell’s tab completion to navigate a directory full of similarly‑named files (many starting with pwncollege) and complete the filename for the real flag file, then cat it to get the flag.

***

## My solve
**Flag:** `pwn.college{Eblf8r2TIaNB7gQMDwqnWCPjnQu.0lN0EzNxwCNzEzNzEzW}`

I started tab-completing from /challenge/files/pwn, inspected the options the shell listed, narrowed down with more typing (pwncollege-fla), and then completed the filename to /challenge/files/pwncollege-flag and read it using cat to get the flag.
```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{Eblf8r2TIaNB7gQMDwqnWCPjnQu.0lN0EzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that when multiple matches exist during tab completion, the shell will stop at the common prefix and either show options (on a second press of Tab) or cycle through them depending on configuration.

***

## References 
*No references used*