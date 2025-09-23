# Pondering Paths

## Position yet Elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$

This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{EuOg3VFw1eYgNb_83_yecKpvvNp.QX4QTN0wSM4AzNzEzW}`

First we invoked the command of the path that was given then it responded with incorrect path and gave the correct path (as in the challenge it is mentioned to find the correct path like this only) . Then I changed my current directory to tmp path which it gave and then again ran /challenge/run which gave the flag.

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EuOg3VFw1eYgNb_83_yecKpvvNp.QX4QTN0wSM4AzNzEzW}
```

### New Learnings
Learned about changing directories and paths.

### References 
No references used.



