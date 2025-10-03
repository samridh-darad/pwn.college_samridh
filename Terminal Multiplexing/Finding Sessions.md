# Terminal Muliplexing

## Finding Sessions
Time for some screen detective work!

If you become an avid screen user, you will inevitably end up with multiple sessions running. How do you find the right one to reattach to?

Well, we can list them:

hacker@dojo:~$ screen -ls
There are screens on:
        23847.mysession   (Detached)
        23851.goodwork    (Detached)
        23855.morework    (Detached)
3 Sockets in /run/screen/S-hacker.
The identifiers of the sessions are the PID of each respective screen process, a dot, and the name of the screen session. To attach to a specific one, you use its name or its PID by giving it as an argument to screen -r.

hacker@dojo:~$ screen -r goodwork
In this challenge, we've created three screen sessions for you. One of them contains the flag. The other two are decoys!

You'll need to check each one until you find it. Don't forget to detach (Ctrl-A d) before trying the next session!

### Solve
**Flag:** `pwn.college{MBYk2r4UTNhU9920hHLTki3xACc.01N4IDOxwSM4AzNzEzW}`

Checked list of detached screen, opened first one and luckily got the flag in that.

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen  -ls
There are screens on:
        144.session_35a9e572e02c1ef7    (Detached)
        147.session_1e7949d0738e7304    (Detached)
        150.session_c6620650ca781655    (Detached)
7 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144
[detached from 144.session_35a9e572e02c1ef7]
In Screen:
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{MBYk2r4UTNhU9920hHLTki3xACc.01N4IDOxwSM4AzNzEzW}
pwn.college{MBYk2r4UTNhU9920hHLTki3xACc.01N4IDOxwSM4AzNzEzW}
```

### New Learnings
Learned to reattach screen using it's name or PID.

### References 
No references used.
