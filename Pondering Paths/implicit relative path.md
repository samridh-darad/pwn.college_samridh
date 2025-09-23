# Pondering Paths

## implicit relative path
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. Here, things get slightly tricky.

Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:

hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ run

This will not invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:

bash: run: command not found

We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!

### Solve
**Flag:** `pwn.college{caj1RYn2TMHFFwkAQ-sT7ZpC_uT.QXxUTN0wSM4AzNzEzW}`

First changed my directory as given in the challenge and then used '.' to use relative path because linux doesn't allow naked paths directly as system files can also be exeucted by that.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{caj1RYn2TMHFFwkAQ-sT7ZpC_uT.QXxUTN0wSM4AzNzEzW}
```

### New Learnings
Learned that linux doesnot allow to use naked path so, '.' can be used to call the same directory again to confirm that we explicitly want to execute the program in the current directory using '.' .

### References 
No references used.



