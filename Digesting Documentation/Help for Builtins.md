# Digesting Documentation

## Help for Builtins
Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. You can get a list of shell builtins by running the builtin help, as so:

hacker@dojo:~$ help
You can get help on a specific one by passing it to the help builtin. Let's look at a builtin that we've already used earlier, cd!

hacker@dojo:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
...
Some good information! In this challenge, we'll practice using help to look up help for builtins. This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

### Solve
**Flag:** `pwn.college{Ey7TSar5bTWXbNnuAdc1S4L3qdq.QX0ETO0wSM4AzNzEzW}`

Since, challenge is a built in command in this program so, used help challenge to know about it's arguments and then used the given argument to get the flag.

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "Ey7TSar5".
hacker@man~help-for-builtins:~$ challenge --secret Ey7TSar5
Correct! Here is your flag!
pwn.college{Ey7TSar5bTWXbNnuAdc1S4L3qdq.QX0ETO0wSM4AzNzEzW}
```

### New Learnings
Learned how to get information about builtin commands where --help and man cannot be used.

### References 
No references used.
