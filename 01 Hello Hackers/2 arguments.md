# Intro to Arguments
The challenge asks us to invoke commands like **echo** and **hello** with different arguments, to get different outputs.

***

## My solve
**Flag:** `pwn.college{YK7oSXU1VuiVzEZLYuDYWI8vNwi.QX4YjM1wCNzEzNzEzW}`

First I invoked the echo commands with different arguments, first a single argument(echo Hello) which outputs the argument(Hello) on the terminal, and then with multiple arguments(echo Hello World) which outputs the arguments(Hello, World) with a one space gap on the terminal. Finally, i invoke the command hello with argument hackers to get the flag.

```
hacker@hello~intro-to-arguments:~$ echo Hello
Hello
hacker@hello~intro-to-arguments:~$ echo Hello World
Hello World
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{YK7oSXU1VuiVzEZLYuDYWI8vNwi.QX4YjM1wCNzEzNzEzW}
```

***

## What I learned
I learnt that Linux commands can be used with *arguments*, where the first word you type is the command and the next words are the arrguments. Arguments are additional data passed to a command which governs the output of the command. I also learnt about the **echo** command which outputs the entered arguments on the terminal.

***

## References 
*No references used*