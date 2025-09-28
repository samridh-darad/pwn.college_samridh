# Practicing Piping

## Redirecting Input
Just like you can redirect output from programs, you can redirect input to programs! This is done using <, as so:

hacker@dojo:~$ echo yo > message
hacker@dojo:~$ cat message
yo
hacker@dojo:~$ rev < message
oy
You can do interesting things with a lot of different programs using input redirection! In this level, we will practice using /challenge/run, which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE! To write that value to the PWN file, recall the prior challenge on output redirection from echo!

### Solve
**Flag:** `pwn.college{EP7BEYhmStihP1QXtMtAfCS-3qk.QXwcTN0wSM4AzNzEzW}`

Redirected stdout of COLLEGE to PWN file and then redirected input of PWN to /challenge/run so, basically content of COLLEGE which had the flag got transferred.

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{EP7BEYhmStihP1QXtMtAfCS-3qk.QXwcTN0wSM4AzNzEzW}
```

### New Learnings
Learned about redirecting inputs using <.

### References 
No references used.
