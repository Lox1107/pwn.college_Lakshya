# Searching For Manuals
The challenge asks us to locate a hidden manpage for the challenge program by using the man database searching features(learned from man man), then run /challenge/challenge with the correct option shown in that manpage to get the flag.

***

## My solve
**Flag:** `pwn.college{EzrEfbpVsmEdaWdbjDd9fi0vEca.QX2EDO0wCNzEzNzEzW}`

I read man man to learn how to search the manpage database, used man --regex challenge to find the randomized manpage entry for the challenge, found the correct option(--zrfbps) then ran /challenge/challenge with the discovered option and argument as 902 to get the flag.
```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man --regex
What manual page do you want?
For example, try 'man man'.
hacker@man~searching-for-manuals:~$ man --regex challenge
hacker@man~searching-for-manuals:~$ /challenge/challenge --zrfbps 902
Correct usage! Your flag: pwn.college{EzrEfbpVsmEdaWdbjDd9fi0vEca.QX2EDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that the man program itself has documentation (man man) which explains how to search the manual database. Using man --regex <pattern> lets you search for manpages by name even when the filename is randomised.
***

## References 
*No references used*