# Deleting characters
The challenge injects some decoy characters(^ and %) into the output flag of /challenge/run and asks us to delete all instances of them using tr -d to get the flag.
***

## My solve
**Flag:** `pwn.college{U_aGSroNSIwsb6F1qFShTvETvm1.0FNxEzNxwCNzEzNzEzW}`

First I ran the /challenge/run program but the flag which was printed had many decoy characters. I then piped that flag through the tr command while using the -d(delete) argument and deleted all the decoy characters(i.e. tr -d ^%) to get the flag.
```
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^w^n^%.%c%o^%l^l^%eg%e^%{^U%_a^G^S^%r^oN%S^%Iw^s%b^6F^1^%q%F^%S%h^%T^%v^E%T^v^%m^%1.%0^%FN%x^Ez^Nx^%w^%C^%N^%zE%z^%Nz%E%z%W^%}^
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{U_aGSroNSIwsb6F1qFShTvETvm1.0FNxEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that we can use tr -d (characters) to remove certain characters from the value sent as input to the tr command. This can be useful when the flag is filled with decoy characters and we need to delete them to get only the flag.

***

## References 
*No references used*