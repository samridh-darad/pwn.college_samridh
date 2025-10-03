#  Chaining Commands

## Executable Shell Scripts
You have written your first shell script, but calling it via bash script.sh is a pain. Why do you need that bash?

When you invoke bash script.sh, you are, of course launching the bash command with the script.sh argument. This tells bash to read its commands from script.sh instead of standard input, and thus your shell script is executed.

It turns out that you can avoid the need to manually invoke bash. If your shell script file is executable (recall File Permissions), you can simply invoke it via its relative or absolute path! For example, if you create script.sh in your home directory and make it executable, you can invoke it via /home/hacker/script.sh or ~/script.sh or (if your working directory is /home/hacker) ./script.sh.

Try that here! Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!

### Solve
**Flag:** `pwn.college{EtPDY8flo14z8gRiAb9quv5O1a9.QX0cjM1wSM4AzNzEzW}`

Created y.sh with /challenge/solve written in it. Changed the shell script permission to executable for everyone, ran it from the home directory directly without using bash command as given in the challenge.

```bash
hacker@chaining~executable-shell-scripts:~$ chmod a+x y.sh
hacker@chaining~executable-shell-scripts:~$ ls -l
total 40
-rw-r--r-x 1 hacker hacker   4 Sep 26 12:18 COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 30 19:06 Desktop
-rw-r--r-x 1 hacker hacker   8 Sep 26 14:58 PWN
-rw-r--r-- 1 root   hacker  60 Sep 23 05:02 h
-rw-r--r-x 1 hacker hacker 829 Sep 26 14:18 instructions
-rw-r--r-- 1 root   hacker  77 Sep 27 06:41 intercept
-rw-r--r-x 1 hacker hacker  95 Sep 26 14:18 myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 24 16:33 not-the-flag -> /flag
-rw-r--r-x 1 hacker hacker 437 Sep 26 14:08 the-flag
-rw-r--r-- 1 hacker hacker  34 Oct  1 18:32 x.sh
-rwxr-xr-x 1 hacker hacker  17 Oct  1 19:13 y.sh
hacker@chaining~executable-shell-scripts:~$ ./y.sh
Congratulations on your shell script execution! Your flag:
pwn.college{EtPDY8flo14z8gRiAb9quv5O1a9.QX0cjM1wSM4AzNzEzW}
```

### New Learnings
Learned to invoke shell scripts without using bash commands by making them executable.

### References 
No references used.
