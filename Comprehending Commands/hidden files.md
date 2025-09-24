# Comprehending Commands

## hidden files
Interestingly, ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag, as so:

hacker@dojo:~$ touch pwn
hacker@dojo:~$ touch .college
hacker@dojo:~$ ls
pwn
hacker@dojo:~$ ls -a
.college	pwn
hacker@dojo:~$

Now, it's your turn! Go find the flag, hidden as a dot-prepended file in /.

### Solve
**Flag:** `pwn.college{4r9cljR3Va2d6kS4UezSrYg40Kg.QXwUDO0wSM4AzNzEzW}`

Changed directory from home to / then used ls -a command to see all the files and even the hidden files which start by '.' . One of the files had flag in it so used cat command to read that file and get the flag.

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.                     bin        etc    lib64   nix   run   tmp
..                    boot       home   libx32  opt   sbin  usr
.dockerenv            challenge  lib    media   proc  srv   var
.flag-46082742522494  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ cat .flag-46082742522494
pwn.college{4r9cljR3Va2d6kS4UezSrYg40Kg.QXwUDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to see the hidden files starting with '.' using ls -a command.

### References 
No references used.

