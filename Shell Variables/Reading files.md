# Shell Variables

## Reading Files
Often, when shell users want to read a file into an environment variable, they do something like:

hacker@dojo:~$ echo "test" > some_file
hacker@dojo:~$ VAR=$(cat some_file)
hacker@dojo:~$ echo $VAR
test
This works, but it represents what grouchy hackers call a "Useless Use of Cat". That is, running a whole other program just to read the file is a waste. It turns out that you can just use the powers of the shell!

Previously, you read user input into a variable. You've also previously redirected files into command input! Put them together, and you can read files with the shell.

hacker@dojo:~$ echo "test" > some_file
hacker@dojo:~$ read VAR < some_file
hacker@dojo:~$ echo $VAR
test
What happened there? The example redirects some_file into the standard input of read, and so when read reads into VAR, it reads from the file! Now, use that to read /challenge/read_me into the PWN environment variable, and we'll give you the flag! The /challenge/read_me will keep changing, so you'll need to read it right into the PWN variable with one command!

### Solve
**Flag:** `pwn.college{QT6whDTNeUa92nW09la3XASNliX.QXwIDO0wSM4AzNzEzW}`

Read in PWN variable and stored the stdin to /challenge/read_me and got the flag.

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QT6whDTNeUa92nW09la3XASNliX.QXwIDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to directly read into variable without using cat command with files.

### References 
No references used.
