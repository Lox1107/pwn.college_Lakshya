# Filtering with grep -v
The challenge asks us to filter the stdout of /challenge/run to remove decoy flags that contain the word DECOY somewhere in them using grep -v(invert match) to get the flag.
***

## My solve
**Flag:** `pwn.college{IDyepWq1s8ABxghPcKIHQ_UhS8_.0FOxEzNxwCNzEzNzEzW}`

I piped the output of /challenge/run into grep -v DECOY to remove decoy flags and get only the real flag.
```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{IDyepWq1s8ABxghPcKIHQ_UhS8_.0FOxEzNxwCNzEzNzEzW}
```

***

## What I learned
I  learned that the -v(invert match) option of the grep command prints only lines that do not match the given pattern, so it’s useful for removing fake or decoy flags from the output.

***

## References 
*No references used*