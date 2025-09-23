# Pondering Paths

## explicit relative paths, from /
Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:

/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
The following relative paths are also all identical to each other:

challenge
./challenge
./././challenge
challenge/.
Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths. Get ready!

### Solve
**Flag:** `pwn.college{oL0ob-SydCCR-2afS4HvDqNcwiB.QXwUTN0wSM4AzNzEzW}`

First the challenge told about the path being naked before and '.' refers to the same directory so, basically we had to first change our directory to the absolute path then use '.' to use the same path with challenge/run as '.' refers to the same directory so using it again is the same thing as using absolute path only once. 

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./run
bash: ./run: Is a directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{oL0ob-SydCCR-2afS4HvDqNcwiB.QXwUTN0wSM4AzNzEzW}
```

### New Learnings
Learned that paths need not be naked and can be expressed in terms of '.' also. Also learned how to use absolute and relative paths with '.' The '.' symbol refers to the same directory

### References 
No references used.




