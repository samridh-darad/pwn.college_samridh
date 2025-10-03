# Terminal Multiplexing

## Launching Screen
Let's dive right in!

screen is a program that creates virtual terminals inside your terminal. It's somewhat like having multiple browser tabs, but for your command line!

Starting screen is super simple:

hacker@dojo:~$ screen
That's it! You're now inside a screen session. It looks exactly like a terminal, but there are new capabilities there, waiting to be discovered.

For this challenge, we've hooked things up so that just launching screen will get you the flag. Easy!

NOTE: When you're done with your command line, type exit or press Ctrl-D to leave the screen session. Then screen will terminate and return you to your original shell.

### Solve
**Flag:** `pwn.college{kg3-K2I_RGT2rEPAmyitFzPhwOq.0VN4IDOxwSM4AzNzEzW}`

Typed screen command in the shell to open a screen and got the flag when exited it.

```bash
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{kg3-K2I_RGT2rEPAmyitFzPhwOq.0VN4IDOxwSM4AzNzEzW}
```

### New Learnings
Learned to lauch a screen and that it's like multiple tabs in a browser.

### References 
No references used.
