# Comprehending Commands

## moving files
You can also move files around with the mv command. The usage is simple:

hacker@dojo:~$ ls
my-file
hacker@dojo:~$ cat my-file
PWN!
hacker@dojo:~$ mv my-file your-file
hacker@dojo:~$ ls
your-file
hacker@dojo:~$ cat your-file
PWN!
hacker@dojo:~$

This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

### Solve
**Flag:** `pwn.college{Yyb2zzmMdQ1YCI45oc5woEhbKfz.0VOxEzNxwSM4AzNzEzW}`

Moved the file from /flag to /tmp/hack-the-planet using mv command and then checked it using /challenge/check in the home directory which gave the flag.

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{Yyb2zzmMdQ1YCI45oc5woEhbKfz.0VOxEzNxwSM4AzNzEzW}
```

### New Learnings
Learned how to move files from one place to another.

### References 
No references used.
