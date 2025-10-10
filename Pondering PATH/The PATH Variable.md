# Pondering PATH

## The PATH Variable
It turns out that the answer to "How does the shell find ls?" is fairly simple. There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands. If you blank out the variable, things go badly:

hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ PATH=""
hacker@dojo:~$ ls
bash: ls: No such file or directory
hacker@dojo:~$
Without a PATH, bash cannot find the ls command.

In this level, you will disrupt the operation of the /challenge/run program. This program will DELETE the flag file using the rm command. However, if it can't find the rm command, the flag will not be deleted, and the challenge will give it to you! Thus, you must make it so that /challenge/run also can't find the rm command!

Keep in mind: /challenge/run will be a child process of your shell, so you must apply the concepts you learned in Shell Variables to mess with its PATH variable! If you don't succeed, and the flag gets deleted, you will need to restart the challenge to try again!

### Solve
**Flag:** `pwn.college{4U2-KK_KzhusLcVQZ-kpFICwoyQ.QX2cDM1wSM4AzNzEzW}`

Blanked the path so that shell cannot find the path to the directories where the program of commands are stored which includes rm command used to remove  files so, it cannot remove flag file and gave it.

```bash
hacker@path~the-path-variable:~$ PATH=" "
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{4U2-KK_KzhusLcVQZ-kpFICwoyQ.QX2cDM1wSM4AzNzEzW}
```

### New Learnings
Learned about PATH of all the commands and how to manipulate it for given conditions.

### References 
No references used.
