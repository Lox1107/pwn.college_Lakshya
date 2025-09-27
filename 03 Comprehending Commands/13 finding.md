# finding files
The challenge asks us to locate a file named flag somewhere on the filesystem using the find command and then read the correct one. Some flag files are decoys or inaccessible, so we can try all matches until we find the correct one.

***

## My solve
**Flag:** `pwn.college{4bYYoxJ3aQL_lOIxUnQRzaAm5FC.QXyMDO0wCNzEzNzEzW}`

I searched the whole filesystem for files named flag, inspected the matches until I found the one containing the real flag, and used cat to get the flag.
```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/javascript/three/examples/jsm/misc/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/root’: Permission denied
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
^C
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/share/javascript/three/examples/jsm/misc/flag
pwn.college{4bYYoxJ3aQL_lOIxUnQRzaAm5FC.QXyMDO0wCNzEzNzEzW}
```

***

## What I learned
I learned how to use find to search directories recursively (for example find / -name flag) and that permission errors can occur when using the find command, they can be ignored while hunting for the file. When multiple matching filenames exist, we must inspect all matches to find the correct one.
***

## References 
*No references used*