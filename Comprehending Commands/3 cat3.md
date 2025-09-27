# more catting practice
The challenge asks us to retrieve a flag file by its absolute path without changing directories.

***

## My solve
**Flag:** `pwn.college{giltyIsbEe1Aut2cL4w8WJlN1Fy.QXwITO0wCNzEzNzEzW}`

Changing directories was not allowed in this challenge so I used cat with the full absolute path of the flag file and read it without using cd to get the flag.
```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /lib/debug/flag. Go cat it out **without** cding into that 
directory!
hacker@commands~more-catting-practice:~$ cat /lib/debug/flag
pwn.college{giltyIsbEe1Aut2cL4w8WJlN1Fy.QXwITO0wCNzEzNzEzW}
```

***

## What I learned
I learned that you can read any file using cat by entering its absolute path as an argument whether or not your current working directory is the same as the one in which the file is present in. So cat can access any file in the entire filesystem using its absolute path as long as we have the permissions.

***

## References 
*No references used*