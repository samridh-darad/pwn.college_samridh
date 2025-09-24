# Comprehending Commands

## removing files
Files are all around you. Like candy wrappers, there'll eventually be too many of them. In this level, we'll learn to clean up!

In Linux, you remove files with the rm command, as so:

hacker@dojo:~$ touch PWN
hacker@dojo:~$ touch COLLEGE
hacker@dojo:~$ ls
COLLEGE     PWN
hacker@dojo:~$ rm PWN
hacker@dojo:~$ ls
COLLEGE
hacker@dojo:~$

Let's practice. This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag!

### Solve
**Flag:** `pwn.college{seEacJjpMqQ8S_ybuWsIPt-Nu3P.QX2kDM1wSM4AzNzEzW}`

Listed all the files in the home directory then used the rm command to delete the file name 'delete_me'. Used the command /challenge/check an got the flag.

```bash
hacker@commands~removing-files:~$ ls
delete_me  h
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{seEacJjpMqQ8S_ybuWsIPt-Nu3P.QX2kDM1wSM4AzNzEzW}
```

### New Learnings
Learned how to remove files from the directories using rm command.

### References 
No references used.
