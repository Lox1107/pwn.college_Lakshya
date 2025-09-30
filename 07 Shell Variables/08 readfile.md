# Reading Files
The challenge asks us to read the contents of /challenge/read_me directly into the variable PWN by using the read command to redirect the contents to get the flag.
***

## My solve
**Flag:** `pwn.college{Yt56wqa0L_i9n23PcEUWSA8GVE8.QXwIDO0wCNzEzNzEzW}`

I used read PWN </challenge/read_me to redirect the contents of the file to read which then stores it into the variable PWN to get the flag.
```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Yt56wqa0L_i9n23PcEUWSA8GVE8.QXwIDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that we can redirect a file's contents straight into read using < filename to put the contents into a variable directly. This avoids the usage of an extra command like cat and avoid usage of command substitution, making it more efficient.

***

## References 
*No references used*