# Terminal Multiplexing

## Detaching and Attaching
Now we'll start digging in with the magic of detaching!

Imagine you're working on something important over a remote connection, and your connection drops. With a normal terminal (outside of this awesome dojo environment), everything's gone. With screen, your work keeps running, and you can reattach later!

You can also detach on purpose, which we'll do in this challenge. You detach by pressing Ctrl-A, followed by d (for detach). This leaves your session running in the background while you return to your normal terminal.

hacker@dojo:~$ screen
[doing some work...]
[Press Ctrl-A, then d]
[detached from 12345.pts-0.hostname]
hacker@dojo:~$ 
To reattach, you can use the -r argument to screen:

hacker@dojo:~$ screen -r
For this challenge, you'll need to:

Launch screen
Detach from it.
Run /challenge/run (this will secretly send the flag to your detached session!)
Reattach to see your prize
FUN FACT: Ctrl-A is screen's activation key for all of its shortcuts in its default configuration. All screen functionality is activated by some command combination starting with Ctrl-A.

HINT: Remember: Hold Ctrl and press A, then release both and press d.

HINT: If you see [detached from...], you did it right!

### Solve
**Flag:** `pwn.college{Iyj06BCkDeTxSKiV1Ny8hkOHkAA.0lN4IDOxwSM4AzNzEzW}`

Opened screen on terminal, detached from it, typed /challenge/run on terminal which sent the flag to the screen then reattached to the screen again using screen -r command.

```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 139.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 139.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
Remove dead screens with 'screen -wipe'.
[detached from 139.pts-0.terminal-multiplexing~detaching-and-attaching]
In screen:
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{Iyj06BCkDeTxSKiV1Ny8hkOHkAA.0lN4IDOxwSM4AzNzEzW}
Yes! Flag is: pwn.college{Iyj06BCkDeTxSKiV1Ny8hkOHkAA.0lN4IDOxwSM4AzNzEzW}
```

### New Learnings
Learned to deattach and reattach to screen because it has more advantages and work remian stored in it.

### References 
No references used.
