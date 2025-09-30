# Grepping errors
The challenge asks us to pipe the program’s stderr into grep so we can search the stderr for the flag.
***

## My solve
**Flag:** `pwn.college{o2XjKHZDhjYn00WE8dS0sG6mC4t.QX1ATO0wCNzEzNzEzW}`

I redirected /challenge/run's stderr into stdout and piped the result to grep with search pattern as pwn.college to get the flag.
```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{o2XjKHZDhjYn00WE8dS0sG6mC4t.QX1ATO0wCNzEzNzEzW}
```

***

## What I learned
I learned that 2>& 1 redirects stderr to where stdout is stored, we can then use | to pipe that new stdout value(stderr) into another program.

***

## References 
*No references used*