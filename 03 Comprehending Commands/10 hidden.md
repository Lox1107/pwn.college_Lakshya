# hidden files
The challenge asks us to locate a flag hidden as a dot‑prefixed(i.e. file name starting with .) file in the root directory. Since files that begin with . are hidden by default, we must list the root directory with ls -a.

***

## My solve
**Flag:** `pwn.college{QowcZZfZ2-CxPgZzFIHmkEfi3Ee.QXwUDO0wCNzEzNzEzW}`

I listed the root directory with ls / -a to reveal hidden files, found the dot-prefixed flag file, and then used cat to read it.
```
hacker@commands~hidden-files:~$ ls / -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-236102736015365  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-236102736015365
pwn.college{QowcZZfZ2-CxPgZzFIHmkEfi3Ee.QXwUDO0wCNzEzNzEzW}
```

***

## What I learned
I learned that files beginning with . are hidden from normal ls command output and that using ls -a reveals the hidden files which may contain important information(like the flag in this case).
***

## References 
*No references used*