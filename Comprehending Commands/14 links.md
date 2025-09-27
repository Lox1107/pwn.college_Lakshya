# linking files
The challenge asks us to use a symbolic link so that the /challenge/catflag program, which reads /home/hacker/not-the-flag, will instead return the real flag stored at /flag.

***

## My solve
**Flag:** `pwn.college{4Xr7bvESDnKn-9mjPxWmgrd7fbd.QX5ETN1wCNzEzNzEzW}`

I created a symbolic link from /flag to /home/hacker/not-the-flag and then ran /challenge/catflag, which read the flag through the symlink.
```
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{4Xr7bvESDnKn-9mjPxWmgrd7fbd.QX5ETN1wCNzEzNzEzW}
```

***

## What I learned
I learned that a symbolic link is like a shortcut that points to another file. When you open the shortcut, the system follows it to the real file and reads that instead. You make one with ln -s target linkname (the real file first, then the shortcut). A symbolic link stores the relative path to the target file.
***

## References 
*No references used*