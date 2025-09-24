# Comprehending Commands

## more catting practice
You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is.

### Solve
**Flag:** `pwn.college{QO2-v97_OYuQ5WodABfTje9WMze.QXwITO0wSM4AzNzEzW}`

Same though process as used in catting absolute paths, i.e used absolute path given in command line with cat to get the flag.

```bash
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/share/ImageMagick-6/flag. Go cat it out **without** cding into
that directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/ImageMagick-6/flag
pwn.college{QO2-v97_OYuQ5WodABfTje9WMze.QXwITO0wSM4AzNzEzW}
```

### New Learnings
Learned to use absolute paths with cat

### References 
No references used.