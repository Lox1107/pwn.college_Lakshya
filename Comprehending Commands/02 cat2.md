# calling absolute paths
The challenge asks us to read the flag file that is stored at the absolute path /flag by passing the absolute path as an argument for cat.

***

## My solve
**Flag:** `pwn.college{MJun9uy-dNDUZaBKU2dwjHzAEf8.QX5ETO0wCNzEzNzEzW}`

I used the cat command on the the absolute path of flag(/flag) to get the flag.
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{MJun9uy-dNDUZaBKU2dwjHzAEf8.QX5ETO0wCNzEzNzEzW}
```

***

## What I learned
I learned that cat can accept absolute paths as arguments, so you can read files stored anywhere on the filesystem by specifying their absoulute path given you have the permission to access it.

***

## References 
*No references used*