# Terminal Multiplexing

## Detaching and Attaching (tmux)
Let's try the same thing with tmux!

tmux (terminal multiplexer) is screen's younger, more modern cousin. It does all the same things but with some different key bindings. The biggest difference? Instead of Ctrl-A, tmux uses Ctrl-B as its command prefix.

So to detach from tmux, you press Ctrl-B followed by d.

hacker@dojo:~$ tmux
[doing some work...]
[Press Ctrl-B, then d]
[detached (from session 0)]
hacker@dojo:~$ 
The commands also differ:

tmux ls - List sessions
tmux attach or tmux a - Reattach to session
For this challenge:

Launch tmux
Detach from it.
Run /challenge/run (this will send the flag to your detached session!)
Reattach to see your prize

### Solve
**Flag:** `pwn.college{Ik-8XxXM0LOZUCmdY9I1s23WaL5.0VO4IDOxwSM4AzNzEzW}`

Launched tmux, detached from it, ran /challenge/run which sent the flag in tmux then reattached again to tmux to get the flag.

```bash
In tmux:
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{Ik-8XxXM0LOZUCmdY9I1s23WaL5.0VO4IDOxwSM4AzNzEzW}
Congratulations, here is your flag: pwn.college{Ik-8XxXM0LOZUCmdY9I1s23WaL5.0VO4IDOxwSM4AzNzEzW}

In terminal:
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
[detached (from session 0)]
```

### New Learnings
Learned about operations of tmux and that it's just like a screen but it's shortcuts start with ctrl-B instead of ctrl-A.

### References 
No references used.
