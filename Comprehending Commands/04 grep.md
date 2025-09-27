# grepping for a needle in a haystack
The challenge asks us to search a large text file for the flag by using grep to find lines that contain the flag’s starting part(i.e. pwn.college).

***

## My solve
**Flag:** `pwn.college{cMc3Cl1NuTF0txSJdVus6KH6jeL.QX3EDO0wCNzEzNzEzW}`

I used grep to search /challenge/data.txt with the flag prefix as the search string to get the flag.
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{cMc3Cl1NuTF0txSJdVus6KH6jeL.QX3EDO0wCNzEzNzEzW}
```

***

## What I learned
I learned how to use grep to search files for specific strings: invoking grep SEARCH_STRING /path/to/file scans the file and prints only the lines that contain the search string. This is useful when working with files which are of very large size.
***

## References 
*No references used*