# Untangling Users

## Other user with su
With no arguments, su will start a root shell (after authenticating with root's password). However, you can also give a username as an argument to switch to that user instead of root. For example:

hacker@dojo:~$ su some-user
Password:
some-user@dojo:~$
Awesome! In this level, you must switch to the zardus user and then run /challenge/run. Zardus' password is dont-hack-me. Good luck!

### Solve
**Flag:** `pwn.college{w2yBlcZfmJrD-SCFzM6YSJfb672.QX2UDN1wSM4AzNzEzW}`

Changed username from root to zardus and then ran /challenge/run in root to get the flag.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{w2yBlcZfmJrD-SCFzM6YSJfb672.QX2UDN1wSM4AzNzEzW}
zardus@users~other-users-with-su:/home/hacker$
```

### New Learnings
Learned how to change usernames instad of keeping it as root.

### References 
No references used.
