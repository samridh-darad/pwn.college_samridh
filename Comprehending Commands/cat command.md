# Comprehending Commands

## cat: not the pet, but the command!
One of the most critical Linux commands is cat. cat is most often used for reading out files, like so:

hacker@dojo:~$ cat /challenge/DESCRIPTION.md
One of the most critical Linux commands is `cat`.
`cat` is most often used for reading out files, like so:

cat will concatenate (hence the name) multiple files if provided multiple arguments. For example:

hacker@dojo:~$ cat myfile
This is my file!
hacker@dojo:~$ cat yourfile
This is your file!
hacker@dojo:~$ cat myfile yourfile
This is my file!
This is your file!
hacker@dojo:~$ cat myfile yourfile myfile
This is my file!
This is your file!
This is my file!

Finally, if you give no arguments at all, cat will read from the terminal input and output it. We'll explore that in later challenges...

In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!

### Solve
**Flag:** `pwn.college{saQnc777saLJbNVialR57PQxck_.QXxcTN0wSM4AzNzEzW}`

In this challenge I used the cat command to read the flag from the flag file which was there inside my home directory and got the flag.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat / ~/flag
cat: /: Is a directory
pwn.college{saQnc777saLJbNVialR57PQxck_.QXxcTN0wSM4AzNzEzW}
```

### New Learnings
Learned how to concatenate two files and how to read from files using cat command.

### References 
No references used.



