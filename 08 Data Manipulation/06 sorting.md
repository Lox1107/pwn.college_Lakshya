# Sorting data
The challenge gives us a file(/challenge/flags.txt) which contains 100 fake flags and one real flag. Also, when the file is sorted alphabetically, the real flag ends up at the bottom of the output. The challenge asks us to use the sort command on the file to get the flag.
***

## My solve
**Flag:** `pwn.college{07lRODo5znbxdk0_HN_sb9OdKEx.0FM0MDOxwCNzEzNzEzW}`

Since the flag appears the last in alphabetical order sorting, i used sort -r on the file so that the flag would appear as the first line in the reverse alphabetical order output, i then read only the firsts line by piping the sorted files through the head command and reading only the firt line(i.e head -n 1) to get the flag.
```
hacker@data~sorting-data:~$ sort -r /challenge/flags.txt | head -n 1
pwn.college{07lRODo5znbxdk0_HN_sb9OdKEx.0FM0MDOxwCNzEzNzEzW}
```

***

## What I learned
I  learned that we can use > to redirect the output of a command to another file.

***

## References 
*No references used*