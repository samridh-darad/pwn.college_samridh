# Pondering Paths

## Program and absolute paths
Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn, in the / directory. If you invoke the challenge correctly, it will give you the flag. Good luck!

### Solve
**Flag:** `pwn.college{slUlW_ueKsiuodeHGT0zSVEtP_0.QX1QTN0wSM4AzNzEzW}`

This challenge was same as previous one, only the path was little bit more complicated to get the flag.

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{slUlW_ueKsiuodeHGT0zSVEtP_0.QX1QTN0wSM4AzNzEzW}
```

### New Learnings
learned more about file paths and absolute file paths.

### References 
No references used.



