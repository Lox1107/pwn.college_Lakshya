# Redirectign more output
The challenge asks us to redirect the standard output of the /challenge/run program to a file named myflag and then read it to get the flag.
***

## My solve
**Flag:** `pwn.college{o2-J0B1Mny78Y0-uXT3FGMK6lFy.QX1YTN0wCNzEzNzEzW}`

I ran the /challenge/run program and redirected its stdout to myflag. Then I used cat on myflag to get the flag.
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{o2-J0B1Mny78Y0-uXT3FGMK6lFy.QX1YTN0wCNzEzNzEzW}
```

***

## What I learned
I  learned that standard output(stdout) and standard error(stderr) are separate output streams and only stdout is redirected using >. This is why i still got the info of the run program on the terminal because it was printed oout using stderr.

***

## References 
*No references used*