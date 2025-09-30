# Redirecting errors
The challenge asks us to run /challenge/run while redirecting its stdout to myflag and its stderr to instructions and then read the flag from myflag.
***

## My solve
**Flag:** `pwn.college{8bY59aQ7GQybDfaMLy2GdqOlfqx.QX3YTN0wCNzEzNzEzW}`

I ran /challenge/run and redirected stdout to myflag and stderr to instructions, then read both files.
```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{8bY59aQ7GQybDfaMLy2GdqOlfqx.QX3YTN0wCNzEzNzEzW}
```

***

## What I learned
I  learned file descriptors 0, 1, and 2 are used for stdin, stdout, and stderr. You redirect them with n>file where n is the FD number. To capture errors, we can use 2>.

***

## References 
*No references used*