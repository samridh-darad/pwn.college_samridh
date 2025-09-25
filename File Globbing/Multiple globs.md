# File Globbing

## Muultiple Globs
So far, you've specified one glob at a time, but you can do more! Bash supports the expansion of multiple globs in a single word. For example:

hacker@dojo:~$ cat /*fl*
pwn.college{YEAH}
hacker@dojo:~$
What happens above is that the shell looks for all files in / that start with anything (including nothing), then have an f and an l, and end in anything (including ag, which makes flag).

Now you try it. We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

### Solve
**Flag:** `pwn.college{YzoEfesY988KPJC5s916v6FK93V.0lM3kjNxwSM4AzNzEzW}`

Used *p* as argument because it will contain everything that starts and ends with p and also everything which has p in between.

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{YzoEfesY988KPJC5s916v6FK93V.0lM3kjNxwSM4AzNzEzW}
```

### New Learnings
Learned about using multiple globs in single command.

### References 
No references used.
