# Comprehending Commands

## touching files
Of course, you can also create files! There are several ways to do this, but we'll look at a simple command here. You can create a new, blank file by touching it with the touch command:

hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ touch pwnfile
hacker@dojo:/tmp$ ls
pwnfile
hacker@dojo:/tmp$

It's that simple! In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag!

### Solve
**Flag:** `pwn.college{AwSIRUUMwvKfLP4bIoxKkKOi9VN.QXwMDO0wSM4AzNzEzW}`

Changed the current directory to /tmp then created two files using touch command in that directory and then invoked /challenge/run in home directory to get the flag.

```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ cd ~
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{AwSIRUUMwvKfLP4bIoxKkKOi9VN.QXwMDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to create files using touch commands.

### References 
No references used.
