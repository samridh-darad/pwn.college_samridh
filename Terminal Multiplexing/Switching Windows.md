# Module Name

## Challenge Name
Add challenge description here

### Solve
**Flag:** `pwn.college{sC40HjqwXU9CjpcpI-_PQCOcVJr.0FO4IDOxwSM4AzNzEzW}`

Reattached to screen, window 1 opened by default then switched to window 0 and got the flag.

```bash
Window 0:
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{sC40HjqwXU9CjpcpI-_PQCOcVJr.0FO4IDOxwSM4AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{sC40HjqwXU9CjpcpI-_PQCOcVJr.0FO4IDOxwSM4AzNzEzW}

Window 1:
 cat <<MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Welcome to the window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-A 0 to switch to window 0!
> MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!

Terminal:
hacker@terminal-multiplexing~switching-windows:~$ screen -r
```

### New Learnings
Learned about operations of window in screen in terminal.

### References 
No references used.
