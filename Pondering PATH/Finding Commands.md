# Pondering PATH

## Finding Commands
When you type the name of a command, something inside one of the many directories listed in your $PATH variable is what actually gets executed (of course, unless the command is a builtin!). But which file, precisely? You can find out with the aptly-named which command:

hacker@dojo:~$ which cat
/bin/cat
hacker@dojo:~$ /bin/cat /flag
YEAH
hacker@dojo:~$
Mirroring what the shell does when searching for commands, which looks at each directory in $PATH in order and prints the first file it finds whose name matches the argument you passed.

In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!

### Solve
**Flag:** `pwn.college{MzvAxiUwgUb7fp9E94fI1JzyNku.01NzEzNxwSM4AzNzEzW}`

Searched the path of the win command using which command which gave the directory of the flag file as it was given in the challenge that it was in the same directory as win command the used that directory  with /flag to get the flag.

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/1377/win
hacker@path~finding-commands:~$ cat /challenge/paths/1377/flag
pwn.college{MzvAxiUwgUb7fp9E94fI1JzyNku.01NzEzNxwSM4AzNzEzW}
```

### New Learnings
Learned to find path of directories in PATH using which command.

### References 
No references used.
