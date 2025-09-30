# Printing Exported Variables
The challenge asks us to run the env command to get the flag.
***

## My solve
**Flag:** `pwn.college{InNhDtTk3Q0mUGK8_PmRFe3uY1i.QX4UTN0wCNzEzNzEzW}`

i ran the env command to print out all exported variable and found the FLAG variable in the output to get the flag.
```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=acae6f934c137914d4081e84e716b73ba3a71d05609560e0a639d59ae922c31d
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{InNhDtTk3Q0mUGK8_PmRFe3uY1i.QX4UTN0wCNzEzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

***

## What I learned
I learned that running env prints out the value of all exported shell variables.

***

## References 
*No references used*