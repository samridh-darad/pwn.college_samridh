# Comprehending Commands

## listing files
So far, we've told you which files to interact with. But directories can have lots of files (and other directories) inside them, and we won't always be here to tell you their names. You'll need to learn to list their contents using the ls command!

ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. Observe:

hacker@dojo:~$ ls /challenge
run
hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ ls /home/hacker
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$

In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.

### Solve
**Flag:** `pwn.college{UFWsg2bdSD6cnAZxXpR2jHrh68p.QX4IDO0wSM4AzNzEzW}`

Used list command to see the files inside the challenge directory as aked in the challenge and then got the new name of the file in which flag is stored, then used the new name of the file with /challenge to get the flag.

```bash
hacker@commands~listing-files:~$ ls /challenge
6768-renamed-run-22607  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/6768-renamed-run-22607
Yahaha, you found me! Here is your flag:
pwn.college{UFWsg2bdSD6cnAZxXpR2jHrh68p.QX4IDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to use ls(list) command to see the files stored in a directory.

### References 
No references used.
