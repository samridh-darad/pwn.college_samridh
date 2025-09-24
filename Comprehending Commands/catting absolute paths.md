# Comprehending Commands

## catting absolute paths
In the last level, you did cat flag to read the flag out of your home directory! You can, of course, specify cat's arguments as absolute paths:

hacker@dojo:~$ cat /challenge/DESCRIPTION.md
In the last level, you did `cat flag` to read the flag out of your home directory!
You can, of course, specify `cat`'s arguments as absolute paths:
...

In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.

### Solve
**Flag:** `pwn.college{Ahp4Hyi021vFqHkTg-fhbJuyzqn.QX5ETO0wSM4AzNzEzW}`

Instruction of the challenge was to use the cat with absolute path so, I did that to get the flag.

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{Ahp4Hyi021vFqHkTg-fhbJuyzqn.QX5ETO0wSM4AzNzEzW}
```

### New Learnings
Learned to use absolute path with cat.

### References 
No references used.
