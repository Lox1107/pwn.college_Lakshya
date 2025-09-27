# comparing files
The challenge asks us to compare two files using *diff* to find the single line with the flag that appears only in the file containing the real flag.

***

## My solve
**Flag:** `pwn.college{YOq4w4KylJdE-ICo6Oqk1iOnU-e.01MwMDOxwCNzEzNzEzW}`

I used  the diff command on the two given files and read the added line in the second file to get the flag.
```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
29a30
> pwn.college{YOq4w4KylJdE-ICo6Oqk1iOnU-e.01MwMDOxwCNzEzNzEzW}
```

***

## What I learned
I learned how to use the diff command to compare two files line-by-line. The output also shows exactly what is different between them. In this case diff reported an added line in the second file, and that added line was the real flag.
***

## References 
*No references used*