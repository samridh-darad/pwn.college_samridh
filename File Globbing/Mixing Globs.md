# File Globbing

## Mixing Globs
Now, let's put the previous levels together! We put a few happy, but diversely-named files in /challenge/files. Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!

### Solve
**Flag:** `pwn.college{Y7S5WcpGQpxryvEeSfJZaBps7iJ.QX1IDO0wSM4AzNzEzW}`

Used [cep]* because the files started with c,e and p.

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{Y7S5WcpGQpxryvEeSfJZaBps7iJ.QX1IDO0wSM4AzNzEzW}
```

### New Learnings
Learned using mixing path glob and star glob together.

### References 
No references used.
