# Digesting Documentation

## Searching for Manuals
This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the manpages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right manpage, read the man page manpage by doing: man man!

### Solve
**Flag:** `pwn.college{ohJK5oZvsGsj49O1SFbvAtMkdk3.QX2EDO0wSM4AzNzEzW}`

Looked in manual that man -k can give manual page name for challenge then saw the manual name and used it to get argument which gave the flag.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
ohovssjbvt (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man ohovssjbvt
hacker@man~searching-for-manuals:~$ /challenge/challenge  --ohovss 549
Correct usage! Your flag: pwn.college{ohJK5oZvsGsj49O1SFbvAtMkdk3.QX2EDO0wSM4AzNzEzW}
```

### New Learnings
Learned to Search for Manuals.

### References 
No references used.
