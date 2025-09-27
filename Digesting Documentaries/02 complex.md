# Learning Complex Usage
The challenge asks us to run /challenge/challenge using a complex argument form: pass the --printfile option and give its argument the path to the file you want printed (in this case /flag).

***

## My solve
**Flag:** `pwn.college{w4FBtQ5omQ_Gr-Ny3UwLoCyInpu.QX1ITO0wCNzEzNzEzW}`

I used the --printfile argument of the /challenge/challenge program and gave it /flag as its argument so the program printed the flag.
```
hacker@man~learning-complex-usage:~$ ls /
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{w4FBtQ5omQ_Gr-Ny3UwLoCyInpu.QX1ITO0wCNzEzNzEzW}
```

***

## What I learned
Some command options take their own arguments. Here, --printfile expects a filename right after it; so the correct usage is --printfile <path>. This esssentially means you sometimes pass an argument to an argument, and you must supply the inner value (the file path) exactly where the program expects it.
***

## References 
[Linux Command Options](https://labex.io/questions/what-are-linux-command-options-209739)