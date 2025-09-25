# Digesting Documentation

## Searching Manuals
You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit n to go to the next result and N to go to the previous result. Instead of /, you can use ? to search backwards!

Find the option that will give you the flag by reading the challenge man page.

### Solve
**Flag:** `pwn.college{oUbKcUlEyliRzjqBE2E-RbQu3wm.QX1EDO0wSM4AzNzEzW}`

Accessed manual for challenge and searched for flag using '/' and found the argument to be used to get the flag.

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge --xxmn
bash: /challenge: Is a directory
hacker@man~searching-manuals:~$ /challenge/challenge --xxmn
Initializing...
Correct usage! Your flag: pwn.college{oUbKcUlEyliRzjqBE2E-RbQu3wm.QX1EDO0wSM4AzNzEzW}
```

### New Learnings
Learned different ways of controlling and searching manuals.

### References 
No references used.
