# Processes and Jobs

## Killing Misbehaving Processes
Sometimes, misbehaving processes can interfere with your work. These processes might need to be killed...

In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write your flag. You need to kill this process.

Your general workflow should be:

Check what processes are running.
Find /challenge/decoy in the list and figure out its process ID.
kill it.
Run /challenge/run to get the flag without being overwhelmed by decoys (you don't need to redirect its output; it'll write to the FIFO on its own).
Good luck!

NOTE: You might see a few decoy flags show up even after killing the decoy process. This happens because Linux pipes are buffered: conceptually, they have a sort of length through which data flows, and you might kill the decoy process while data is in the pipe. That data, having already entered the pipe, will proceed to the other end (your cat). If you wait a second, you'll see the decoys stop, and then you can /challenge/run and win!

### Solve
**Flag:** `pwn.college{8ohZfozbwax_LL4mRMbPUkLee-m.0FNzMDOxwSM4AzNzEzW}`

Searched PID of the decoy file to kill them, then ran /challenge/run to transfer real flag to /tmp/flag_fifo and then cat it in other terminal.

```bash
First terminal : 
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:15 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 13:15 ?        00:00:00 /run/dojo/bin/sleep 6h
root         138       1  0 13:15 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 13:15 ?        00:00:00 /bin/bash /challenge/.init
root         140       1  0 13:15 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         141     139  0 13:15 ?        00:00:00 sleep 6h
root         142     138  0 13:15 ?        00:00:00 sleep 6h
hacker       143     140  0 13:15 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       154       1  0 13:15 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       158       0  0 13:15 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       164     158  0 13:15 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       173     154  0 13:15 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       184     164  0 13:17 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 143
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!

Other terminal: 
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{8ohZfozbwax_LL4mRMbPUkLee-m.0FNzMDOxwSM4AzNzEzW}
```

### New Learnings
Learned how to handle misbehaving processes.

### References 
No references used.
