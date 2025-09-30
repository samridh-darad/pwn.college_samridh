# Processes and Jobs

## Resuming Processes
Usually, when you suspend processes, you'll want to resume them at some point. Otherwise, why not just terminate them? To resume processes, your shell provides the fg command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.

Go try it out! This challenge's run needs you to suspend it, then resume it. Good luck!

### Solve
**Flag:** `pwn.college{A0KfGsThe9lBpjrx4uePZjS3oEq.QX2QDO0wSM4AzNzEzW}`

We suspend processes because we need to resume them later on otherwise we'll just kill them so, started /challenge/run process, suspended it and then resumed it with fg command.

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{A0KfGsThe9lBpjrx4uePZjS3oEq.QX2QDO0wSM4AzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

### New Learnings
Learned how to resume processes.

### References 
No references used.
