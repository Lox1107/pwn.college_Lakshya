# Matching paths with []
The challenge asks us to pass a single absolute path argument to /challenge/run that uses a bracket glob so it expands into the four absolute filenames /challenge/files/file_b, /challenge/files/file_a, /challenge/files/file_s, and /challenge/files/file_h.

***

## My solve
**Flag:** `pwn.college{UbGnO7a8dchqW4_9oTcXc9-bo_Q.QX0IDO0wCNzEzNzEzW}`

I invoked the /challenge/run program from the home directory with a single absolute path argument containing a bracket glob that expanded into the required files(i.e. /challenge/files/file_[bash]).
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{UbGnO7a8dchqW4_9oTcXc9-bo_Q.QX0IDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that globs can be used inside full paths too, the shell expands patterns like /challenge/files/file_[bash] into the matching absolute paths before running the command.

***

## References 
*No references used*