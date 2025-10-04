# Translating characters
The challenge asks us to flip the case of each character in the output of /challenge/run using tr to get the flag.
***

## My solve
**Flag:** `pwn.college{gqms72ywQaC2kgVTuLaBjyl2oV7.01MxEzNxwCNzEzNzEzW}`

First I ran the /challenge/run program but the flag which was printed had all the characters case-flipped. I then piped that flag through the tr command while swapping the case of all characters(tr A-Za-z a-zA-z) to get the flag in its correct form.
```
hacker@data~translating-characters:~$ /challenge/run
Your case-swapped flag:
PWN.COLLEGE{GQMS72YWqAc2KGvtUlAbJYL2Ov7.01mXeZnXWcnZeZnZeZw}

hacker@data~translating-characters:~$ /challenge/run | tr A-Za-z a-zA-Z
yOUR CASE-SWAPPED FLAG:
pwn.college{gqms72ywQaC2kgVTuLaBjyl2oV7.01MxEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that the tr command can be used to swap certain characters of the input given to it. It takes two sets of characters as arguments and if any character from the first set is found in the input, it is mapped and converted to the corresponding character in the second set.

***

## References 
*No references used*