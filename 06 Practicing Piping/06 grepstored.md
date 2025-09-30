# Grepping stored results
The challenge asks us to redirect the output of /challenge/run into /tmp/data.txt but the output is very large so it asks us to grep the file for the flag.

## My solve
**Flag:** `pwn.college{kNaT6F7Z6fJQU5jAvEZ4eRQz65T.QX4EDO0wCNzEzNzEzW}`

I redirected the program’s stdout into /tmp/data.txt and then used grep on the file with the search pattern as pwn.college to find the flag.
```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{kNaT6F7Z6fJQU5jAvEZ4eRQz65T.QX4EDO0wCNzEzNzEzW}
```

***

## What I learned
I  learned that when redirecting a large output file, we can use grep to easily find the relevant data from the output(the flag in this case).

***

## References 
*No references used*