# Practicing Piping

## Redirecting Output
First, let's look at redirecting stdout to files. You can accomplish this with the > character, as so:

hacker@dojo:~$ echo hi > asdf
This will redirect the output of echo hi (which will be hi) to the file asdf. You can then use a program such as cat to output this file:

hacker@dojo:~$ cat asdf
hi
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

### Solve
**Flag:** `pwn.college{QxBPDipzD6BxdSk4DBl7KP4TKCS.QX0YTN0wSM4AzNzEzW}`

Used echo which prints the argument given to it in stdout and then used > to redirect it to the given file COLLEGE and got the flag.

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{QxBPDipzD6BxdSk4DBl7KP4TKCS.QX0YTN0wSM4AzNzEzW}
```

### New Learnings
Learned redirecting stdout to files using >.

### References 
No references used.
