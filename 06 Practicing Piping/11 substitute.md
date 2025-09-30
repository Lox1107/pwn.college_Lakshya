# Process substitution for input
The challenge asks us to compare the outputs of two commands directly by using process substitution with diff command to get the flag.
***

## My solve
**Flag:** `pwn.college{0SXX3c229BtHhfb9KmOr53tb4Ic.0lNwMDOxwCNzEzNzEzW}`

I used process substitution so diff could compare the outputs of the two programs to remove the decoys and only get the real flag without using additional files.
```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
15a16
> pwn.college{0SXX3c229BtHhfb9KmOr53tb4Ic.0lNwMDOxwCNzEzNzEzW}
```

***

## What I learned
I learned that <(command) runs the command and returns a file-like path(a named pipe) that contains the command’s stdout. We can put this output into other commands without using temporary files.

***

## References 
*No references used*