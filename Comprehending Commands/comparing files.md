# Comprehending Commands

## comparing files
When looking for changes between similar files, eyeballing them might not be the most efficient approach! This is where the diff command becomes invaluable.

diff compares two files line by line and shows you exactly what's different between them. For example:

hacker@dojo:~$ cat file1
hello
world
hacker@dojo:~$ cat file2
hello
universe
hacker@dojo:~$ diff file1 file2
2c2
< world
---
> universe

The output tells us that line 2 changed (2c2), with world in the first file (<) being replaced by universe in the second file (>).

Sometimes, when new lines are added, you'll see something like:

hacker@dojo:~$ cat old
pwn
hacker@dojo:~$ cat new
pwn
college
hacker@dojo:~$ diff old new
1a2
> college

This tells us that after line 1 in the first file, the second file has an additional line (1a2 means "after line 1 of file1, add line 2 of file2").

Now for your challenge! There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag
Use diff to find what's different between these files and get your flag!

### Solve
**Flag:** `pwn.college{UxucsniVOTT_BnFp3Mg9z4S5Xyi.01MwMDOxwSM4AzNzEzW}`

Since one of the two files had the real flag with all the fake ones being the same so, I used the diff command to get the extra flag which is different than all the fake ones which are same in both the files.
This tells us that after line 93 in the first file, the second file has an additional line (93a94 means "after line 93 of file1, add line 94 of file2").

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
93a94
> pwn.college{UxucsniVOTT_BnFp3Mg9z4S5Xyi.01MwMDOxwSM4AzNzEzW}
```

### New Learnings
Learned how to use diff command to find the difference between data or if some additional data is present of two files.

### References 
No references used.
