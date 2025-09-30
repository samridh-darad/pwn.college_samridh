# Processes and Jobs

## Backgrounding Processes
You've resumed processes in the foreground with the fg command. You can also resume processes in the background with the bg command! This will allow the process to keep running, while giving you your shell back to invoke more commands in the meantime.

This level's run wants to see another copy of itself running, not suspended, and using the same terminal. How? Use the terminal to launch it, then suspend it, then background it with bg and launch another copy while the first is running in the background!

### Solve
**Flag:** `pwn.college{AZgqPJIz1VxyuVMZQ_IVsiabyXF.QX3QDO0wSM4AzNzEzW}`

Ran the file, suspended it and then resumed it in background. After that opened the same file in the foreground so, got two copies of the same file which met the condition and gave the flag.

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         161 S+   bash /challenge/run
root         163 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         161 S    bash /challenge/run
root         171 S    sleep 6h
root         172 S+   bash /challenge/run
root         174 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{AZgqPJIz1VxyuVMZQ_IVsiabyXF.QX3QDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to resume files in background.

### References 
No references used.
