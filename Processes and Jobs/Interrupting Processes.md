# Processes and Jobs

## Interrupting Processes
ou've learned how to kill other processes with the kill command, but sometimes you just want to get rid of the process that's clogging up your terminal! Luckily, terminals have a hotkey for this: Ctrl-C (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.

Try it here! /challenge/run will refuse to give you the flag until you interrupt it. Good luck!

### Solve
**Flag:** `pwn.college{g7zdnyeungGutrEd_COXon8Hn2T.QXzQDO0wSM4AzNzEzW}`

Tried to run /challenge/run but had to interrupt it to get the flag.

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{g7zdnyeungGutrEd_COXon8Hn2T.QXzQDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to interrup process so they can cleanly exit.

### References 
No references used.
