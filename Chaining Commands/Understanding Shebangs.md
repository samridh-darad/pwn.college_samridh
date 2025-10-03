# Chaining Commands

## Understanding Shebangs
You're well on your way to your new life as a shell scripter! However, so far, your shellscripts can only be launched from the shell. Things worked great in the previous level (because you were invoking your script from the bash shell), but they won't work if your script was being invoked by, say, a program written in Python (or any other language).

When a program is invoked in Linux, the Linux kernel first inspects the file to determine how it should be run. This does NOT use the extension (which is why you don't have to name your shell scripts with a .sh extension, or your Python scripts with a .py extension, or so on). Rather, Linux looks at the first few bytes of the file for this information.

There are a bunch of different types of programs, but if the program file starts with the characters #! (often termed a "shebang"), Linux treats the file as an interpreted program, and the contents of the rest of the line as the path to the interpreter. It then invokes the interpreter with the path to the program file as its only argument.

Consider this shell script:

#!/bin/bash

echo "Hello Hackers!"
This can be executed as:

hacker@dojo:~$ chmod a+x script.sh
hacker@dojo:~$ ./script.sh
Hello Hackers!
hacker@dojo:~$
When ./script.sh was executed, Linux opened the file, read the first line, extracted /bin/bash as the interpreter, and executed /bin/bash ./script.sh to launch the script!

Note, the shebang line must be the VERY FIRST line of the file - no blank lines or spaces before it!

For this challenge, create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run /challenge/run to verify your script works correctly!

FUN FACT: Common shebangs you might see:

#!/bin/bash for bash scripts
#!/usr/bin/python3 for Python scripts
#!/bin/sh for POSIX shell scripts --- this is a more primitive predecessor to bash with fewer features, but more compatibility to non-Linux systems!

### Solve
**Flag:** `pwn.college{MWjQVkhWZV7g0zdWFjfuXmA6Kjn.0VOzMDOxwSM4AzNzEzW}`

Opened the shell script, made it a shebang, wrote the commands given in the challenge inside the shell script. After that gave the everyone (owner,group and others) permission of the file to be executable. Ran the shell script on the terminal without using the bash commandand got the flag.  

```bash
hacker@chaining~understanding-shebangs:~$ chmod a+x solve.sh
hacker@chaining~understanding-shebangs:~$ ./solve.sh
hack the planet
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{MWjQVkhWZV7g0zdWFjfuXmA6Kjn.0VOzMDOxwSM4AzNzEzW}
```

### New Learnings
Learned to specify shebangs and the uses of shebangs that it doesn't require bash command, specifies the interpreter and different commands can be written in the start of shell script which is read by linux and then executes the file in that language/manner.

### References 
No references used.
