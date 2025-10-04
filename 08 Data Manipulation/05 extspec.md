# Extracting specific sections of text
The challenge asks us to extract only the column containing the single characters of the flag from the /challenge/run command which returns many lines with numbers and single characters(of the flag) using the cut command and then use tr -d to remove all the newlines from the flag column.
***

## My solve
**Flag:** `pwn.college{svl2uTdppApYdEnxirg0vDplqCM.01NxEzNxwCNzEzNzEzW}`

First I ran the /challenge/run program but it printed many different lines with the second column containing the single characters of the flag. I then piped that output through the cut command with the delimiter as " " and the field number as 2(cut -d " " -f 2). But the output would still be printed across many lines, so i used tr -d "\n" to remove all the newlines from the output and got the flag printed in one single line.
```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
1096 p
9851 w
25664 n
23389 .
24818 c
17816 o
6842 l
14293 l
16638 e
1198 g
26375 e
14754 {
26295 s
12400 v
4695 l
18500 2
27208 u
16447 T
2511 d
31272 p
27112 p
8283 A
24181 p
32337 Y
14021 d
24096 E
3471 n
14305 x
17223 i
11000 r
11812 g
20546 0
8264 v
29946 D
25680 p
19018 l
25601 q
14184 C
8554 M
20643 .
11903 0
16684 1
18523 N
3897 x
31280 E
1313 z
27359 N
29606 x
22153 w
32219 C
15029 N
23508 z
19332 E
1422 z
20035 N
8412 z
27485 E
10064 z
31938 W
15435 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{svl2uTdppApYdEnxirg0vDplqCM.01NxEzNxwCNzEzNzEzW}
```

***

## What I learned
I learned that the cut command can be used to extract specific columns from the input given to it. We can specify the delimiter(the character that separates two columns) using -d and the field(column) number using -f.

***

## References 
*No references used*