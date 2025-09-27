# Matching with []
The challenge asks us to use a bracket glob so a single argument expands to several specific filenames. In this level we need to change our working directory into /challenge/files and run /challenge/run with one argument that uses [] globbing so it matches file_b, file_a, file_s, and file_h to get the flag.

***

## My solve
**Flag:** `pwn.college{E8dnArDQ3F5_3OIja8AoWXPo07y.QXzIDO0wCNzEzNzEzW}`

I changed into /challenge/files and invoked /challenge/run with a bracket glob as an argument that matched the required files(file_[bash]).
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ../run file_[bash]
You got it! Here is your flag!
pwn.college{E8dnArDQ3F5_3OIja8AoWXPo07y.QXzIDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that [...] lets you match exactly one character from a set we list inside the brackets, so file_[bash] expands to file_a file_b file_s file_h when those files exist. Bracket globs are useful when we want to match a specific set of possible characters at a single position in a filename.

***

## References 
*No references used*