# Cracking passwords
The challenge asks us to use john(John The Ripper) on a given leaked /etc/shadow file(i.e. /challenge/shadow-leak) to decrypt(crack) the password for the user zardus, then switch user to zardus using su and runnning /challenge/run to get the flag.
***

## My solve
**Flag:** `pwn.college{MEnod0czkTouBQChdQgu4MDCoYk.QX3UDN1wCNzEzNzEzW}`

First I used John the Ripper tool(john) on the leaked shadow file which contained hashed passwords, then waited for some time. It returned the decrypted(cracked) password for zardus(i.e. aardvark) and then used su to switch user to zardus. Then I ran /challenge/run as zardus to get the flag.
```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:17 100% 2/3 0.05589g/s 325.4p/s 325.4c/s 325.4C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{MEnod0czkTouBQChdQgu4MDCoYk.QX3UDN1wCNzEzNzEzW}
```

***

## What I learned
I learned that the passwords for all users are stored in the /etc/shadow file where the fields are separated by using :. The first field is the username and the second field is the password but the password is stored in a one-way encrytped(hashed) format. * or ! in the password field means that password login is not allowed for the user and a blank password means that there is no password for that user. I also learned how to use the John The Ripper tool to crack these hashed passwords if we have a leaked shadow file.

***

## References 
*No references used*