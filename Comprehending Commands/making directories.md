# Comprehendinng Commands

## making directories
We can create files. How about directories? You make directories using the mkdir command. Then you can stick files in there!

Watch:

hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ mkdir my_directory
hacker@dojo:/tmp$ ls
my_directory
hacker@dojo:/tmp$ cd my_directory
hacker@dojo:/tmp/my_directory$ touch my_file
hacker@dojo:/tmp/my_directory$ ls
my_file
hacker@dojo:/tmp/my_directory$ ls /tmp/my_directory/my_file
/tmp/my_directory/my_file
hacker@dojo:/tmp/my_directory$

Now, go forth and create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag!

### Solve
**Flag:** `pwn.college{8C4w5W9B-3VB1pepPWUS7DyEQ26.QXxMDO0wSM4AzNzEzW}`

Went to the mentioned path and made a directory in it and then made one file in it as stated then finally, checked using the command given /challenge/run to get the flag.

```bash
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{8C4w5W9B-3VB1pepPWUS7DyEQ26.QXxMDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to make directories.

### References 
No references used.
