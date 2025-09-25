# Digesting Documentation

## Helpful Programs
Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually, this argument is --help, but it can often be -h or, in rare cases, -?, help, or other esoteric values like /? (though that latter is more frequently encountered on Windows).

In this level, you will practice reading a program's documentation with --help. Try it out!

### Solve
**Flag:** `pwn.college{helloworld}`

Used /challenge with --help but it was a directory so, used /challenge/challenge with help which gave the arguments to print the number of the flag and the argument to be used with the number of the flag to give the flag.

```bash
hacker@man~helpful-programs:~$ /challenge --help
bash: /challenge: Is a directory
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 830
hacker@man~helpful-programs:~$ /challenge/challenge -g 830
Correct usage! Your flag: pwn.college{wbAALGWdiBKYcqadCANvXFV8tJd.QX3IDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to use --help when programs don't have man page

### References 
No references used.
