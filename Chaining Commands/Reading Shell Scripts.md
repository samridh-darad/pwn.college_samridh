# Chaining Commands

## Reading Shell Scripts
You're not the only one who writes shell scripts! They are very handy for doing simple "system-level" tasks, and are a common tool that developers and sysadmins reach for. In fact, a surprising fraction of the programs on a typical Linux machine are shell scripts.

In this level, we will learn to read shell scripts. /challenge/run is a shell script that requires you to put in a secret password, but that password is hardcoded into the script iself! Read the script (using, say, cat), figure out the password, and get the flag!

NOTE: Feel free to try to read the code of other challenges as well! Reading code is a critical strategy in learning new skills, because you can see how certain functionality was implemented and reuse those strategies in your own scripts. But watch out: some program files are machine code, and will not be readable to humans. You can use the file command to differentiate, but almost all the challenges in the Linux Luminarium are implemented as shell scripts and are safe to cat out.

### Solve
**Flag:** `pwn.college{8sIK74HvpjuQY-zZmOOGRSBE5QY.0lMwgDOxwSM4AzNzEzW}`

Read the shell script using cat statement, the password was written with if condition which will give the flag so, ran /challenge/run in terminal and wrote the password which was "hack the PLANET" and got the flag.

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{8sIK74HvpjuQY-zZmOOGRSBE5QY.0lMwgDOxwSM4AzNzEzW}
```

### New Learnings
Learned to read shell scripts and analyse it's code.

### References 
No references used.
