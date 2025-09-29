# Data Manipulation

## Deleting Characters
tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete:

hacker@dojo:~$ echo PAWN | tr -d A
PWN
hacker@dojo:~$
Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them!

### Solve
**Flag:** `pwn.college{UlB6zub8fgk8ZCCwfFNnRR7cBqf.0FNxEzNxwSM4AzNzEzW}`

Deleted % and ^ characters from the flag to get the flag.

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d '%^'
Your character-stuffed flag:
pwn.college{UlB6zub8fgk8ZCCwfFNnRR7cBqf.0FNxEzNxwSM4AzNzEzW}
```

### New Learnings
Learned hwo to deleted characters using -d argument with tr.

### References 
No references used.
