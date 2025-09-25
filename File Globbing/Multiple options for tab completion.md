# File Globbing

## Multiple options for tab completion
Consider the following situation:

hacker@dojo:~$ ls
flag  flamingo  flowers
hacker@dojo:~$ cat f<TAB>
There are multiple options! What happens?

What happens varies based on the specific shell and its options. By default bash will auto-expand until the first point when there are multiple options (in this case, fl). When you hit tab a second time, it'll print out those options. Other shells and configurations, instead, will cycle through the options.

This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag!



### Solve
**Flag:** `pwn.college{AGRHhbqD2YekXrkLmdSW5ZOhDNW.0lN0EzNxwSM4AzNzEzW}`

Used cat to read the flag with multiple tab completions after pwn.

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{AGRHhbqD2YekXrkLmdSW5ZOhDNW.0lN0EzNxwSM4AzNzEzW}
```

### New Learnings
Learned to use multiple tab completiions.

### References 
No references used.
