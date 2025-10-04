# Extracting the first lines with head
The challenge asks us to pipe only the first 7 lines of the /challenge/pwn program to /challenge/college using the head command to get the flag.
***

## My solve
**Flag:** `pwn.college{oLFV1hQ0TNuKHRYmvqdK9GFyLn3.0lNxEzNxwCNzEzNzEzW}`

The challenge/pwn program prints a lot of lines so I piped its output to the head command to extract only the first 7 lines(head -n 7) and then piped those 7 lines into the /challenge/college command which prints the flag only if it gets those first 7 lines as an input to get the flag.
```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{oLFV1hQ0TNuKHRYmvqdK9GFyLn3.0lNxEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that the head command can be used to read only the first few lines of the input given to it. By default, it reads the first 10 lines but we can use the -n option to specify the number of lines to be read(i.e head -n <number>).

***

## References 
*No references used*